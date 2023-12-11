# copy
## 4. 핵심 기능
우리의 서비스의 핵심기능은 AWS, OCR 및 API를 이용한 그룹 커뮤니티 기능입니다.
사용자는 본인이 원하는 취미를 등록하여 가입하고싶은 그룹에 가입해 그룹원들과
게시글, 사진 공유 및 그룹일정관리 , 회비관리등 을 이용 할 수 있는 사이트입니다.

<details>
<summary><b>핵심 기능 설명 펼치기</b></summary>
<div markdown="1">

### 4.1. 전체 흐름도
![image](https://github.com/chanhyuckkim/copy/assets/149571615/0eb8ff0b-0cdf-46ee-8761-cc1886f75038)


### 4.2. 메인페이지 핵심기능

- **본인 취미에 맞는 그룹 노출** :pushpin: [코드 확인]
- ![image](https://github.com/chanhyuckkim/copy/assets/149571615/59ca12fd-10c1-4fa4-aa7c-fb3757f01928)
(https://github.com/Integerous/goQuality/blob/b587bbff4dce02e3bec4f4787151a9b6fa326319/frontend/src/components/PostInput.vue#L67)(https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/mainpgjs/mainrank.js#L3)
  - 본인이 선택한 취미에 맞는 그룹이 사용자들의 좋아요 갯수가 많은 그룹부터 차례대로 노출됩니다.
  - 취미에 맞는 프로필사진을 AWS에서 불러옵니다.
### 4.3.  커뮤니티 사이트 핵심기능

- **글/사진 등록** :pushpin: [코드 확인]
  ![image](https://github.com/chanhyuckkim/copy/assets/149571615/2f4963a6-c3c2-4436-a1c3-3c0c035a3fc4)

https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/WEB-INF/community.html#L472
  - 그룹별로 커뮤니티사이트에서 게시글과 사진을 등록할 수 있습니다.
    
- **그룹 일정** :pushpin: [코드 확인]
https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/calendar.js#L5C1-L5C1
  - 그룹별로 일정을 등록할수 있습니다.

### 4.4. Service

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_service1.png)

- **Http 프로토콜 추가 및 trim()** :pushpin: [코드 확인]()
  - 사용자가 URL 입력 시 Http 프로토콜을 생략하거나 공백을 넣은 경우,  
  올바른 URL이 될 수 있도록 Http 프로토콜을 추가해주고, 공백을 제거해줍니다.

- **URL 접속 확인** :pushpin: [코드 확인]()
  - 화면단에서 모양새만 확인한 URL이 실제 리소스로 연결되는지 HttpUrlConnection으로 테스트합니다.
  - 이 때, 빠른 응답을 위해 Request Method를 GET이 아닌 HEAD를 사용했습니다.
  - (HEAD 메소드는 GET 메소드의 응답 결과의 Body는 가져오지 않고, Header만 확인하기 때문에 GET 메소드에 비해 응답속도가 빠릅니다.)

  ![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_service2.png)

- **Jsoup 이미지, 제목 파싱** :pushpin: [코드 확인]()
  - URL 접속 확인결과 유효하면 Jsoup을 사용해서 입력된 URL의 이미지와 제목을 파싱합니다.
  - 이미지는 Open Graphic Tag를 우선적으로 파싱하고, 없을 경우 첫 번째 이미지와 제목을 파싱합니다.
  - 컨텐츠에 이미지가 없을 경우, 미리 설정해둔 기본 이미지를 사용하고, 제목이 없을 경우 생략합니다.


### 4.5. Repository

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_repo.png)

- **컨텐츠 저장** :pushpin: [코드 확인]()
  - URL 유효성 체크와 이미지, 제목 파싱이 끝난 컨텐츠는 DB에 저장합니다.
  - 저장된 컨텐츠는 다시 Repository - Service - Controller를 거쳐 화면단에 송출됩니다.

</div>
</details>

</br>
