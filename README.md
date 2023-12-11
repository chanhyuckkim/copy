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

- **본인 취미에 맞는 그룹 노출** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/mainpgjs/mainrank.js#L3)
- ![image](https://github.com/chanhyuckkim/copy/assets/149571615/59ca12fd-10c1-4fa4-aa7c-fb3757f01928)

  - 본인이 선택한 취미에 맞는 그룹이 사용자들의 좋아요 갯수가 많은 그룹부터 차례대로 노출됩니다.
  - 취미에 맞는 프로필사진을 AWS에서 불러옵니다.
### 4.3.  커뮤니티 사이트 핵심기능

- **글/사진 등록** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/WEB-INF/community.html#L472)
  ![image](https://github.com/chanhyuckkim/copy/assets/149571615/2f4963a6-c3c2-4436-a1c3-3c0c035a3fc4)


  - 그룹별로 커뮤니티사이트에서 게시글과 사진을 등록할 수 있습니다.
    
- **그룹 일정** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/calendar.js#L5C1-L5C1)
![image](https://github.com/chanhyuckkim/copy/assets/149571615/406e065b-f434-474d-b3bf-bbb6e9fb4776)

  - 그룹별로 일정을 등록할수 있습니다.
  - 풀캘린더 API를 이용하여 일정관리를 할 수 있습니다.
- **장소 검색** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/map.js#L6)
![image](https://github.com/chanhyuckkim/copy/assets/149571615/19ff317e-7750-4b5c-8f06-4766adfbb504)

- 키워드로 장소를 검색하여 가게 정보를 쉽게 찾아볼 수 있습니다.
- **회비 관리** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/assets/js/feecalendar/feecalendar.js#L3)
![image](https://github.com/chanhyuckkim/copy/assets/149571615/edcd95d1-e644-426b-9772-a9cbe88d83fd)

- 사용한 회비를 입력하여 관리할 수 있습니다.
- OCR기반으로 영수증의 텍스트를 읽어 회비관리를 할 수 있습니다.
  ![image](https://github.com/chanhyuckkim/copy/assets/149571615/f7aeb4f7-d41c-4ece-91fd-720ede2fccba)
- **그룹회원조회** :pushpin: [코드 확인](https://github.com/2023-SMHRD-IS-CLOUD-1/YOU-I/blob/85cf700df6aed74bfe6b06e964702aaf8430bd45/YOU%26I/src/main/webapp/WEB-INF/clubmember.html#L163C1-L163C1)
![image](https://github.com/chanhyuckkim/copy/assets/149571615/df02c5b4-6516-4715-90d8-bfd9c2d38ab8)

- 본인이 속한 그룹의 회원들의 정보를 열람할 수 있습니다.
- 회원가입할때 저장한 사진파일을 AWS를 통해 불러옵니다.
</div>
</details>

</br>
