# 🛍 Spring-Project-Okitchen
식품 판매 쇼핑몰 팀 프로젝트 

------------

# 📝개요

* 프로젝트 명 : Okitchen

## 🗓 프로젝트 기간

2023년 11월 07일 ~ 2023년 11월 29일


## 📢 개발 목적
온라인 식품 쇼핑몰, 판매자가 상품을 등록, 관리자가 누적된 데이터를 활용할 수 있는 사이트 제작


## 🎨 개발 환경

  - Server : Apache-tomcat-9.0.80
  - IDE : STS 3.9
  - Database : Oracle SQL Developer ( version 18.3.0 )
  - Programming Language : JAVA, HTML, CSS, JavaScript, JSP, SQL
  - Framework/flatform : Spring, mybatis, jQuery 3.7.1, Bootstrap v5.3.1x
  - API : Kakao map, coolsms 


------------

# 📝내용


## 🤼‍ 팀원별 역할

  - 공통 : 기획, 요구 사항 정의, DB 설계, 화면 구현
  - 김서영 : 일반 회원 CRUD, 로그인, 상품 검색, 찜하기 
  - 박수진 : 판매자 회원 CRUD, 로그인, 관리자 기능(상품 관리)
  - 신민기 : 커뮤니티 게시판 CRUD, 관리자 (매출 조회,배송 상태 변경)
  - 이주녕 : 장바구니 CRUD, 결제하기 
  - 이초희 : 상품 CRUD, 상품 카테고리 및 상세 조회
  - 전의진 : 상품문의 CRUD , 상품후기 CRUD 

## 💻‍ 구현 기능

  - 회원가입
  - 로그인, 로그아웃
  - 아이디 찾기, 비밀번호 재설정정
  - 상품 검색
  - 찜하기
  - 관리자(회원 조회)

## 📝 ERD  

![image](https://github.com/seo02wow/Okitchen/assets/135966211/77e5f81d-5b27-4bfa-be1a-107c94053aa1)



------------

# 📝구현 기능

## 회원가입

 1. <h3>회원가입</h3>

![회원가입](https://github.com/seo02wow/Okitchen/assets/135966211/6d9a03e7-867e-4717-81fb-bad66a0cc229)



  **회원가입 페이지**
   
  * 구현 기능 설명
    - 아이디 : 7자 이상 16자 이하 입력 , 중복 체크
    - 비밀번호 : 10자 이상 16자리 이하 입력
    - 이메일 : 중복 체크 
    - 주소 : 카카오 주소 API를 이용한 주소 검색 
    - 핸드폰 : 핸드폰 인증 번호 API를 이용한 인증번호 전송 , 중복 체크
    - 생년월일 : 만 14세 이상만 가입 가능
    - DB값 검증 <br>

------------

2. <h3>개인정보 수정</h3>

![회원정보수정](https://github.com/seo02wow/Okitchen/assets/135966211/406ba0a5-eb6a-42e6-881f-f0afb128de7e)

  

**개인정보 수정 페이지**

  * 구현 기능 설명
     - 로그인 시 세션(Session) 생성
     - 개인정보 수정 시, 현재 비밀번호 입력 후 페이지 이동
     - DB에 등록된 회원 정보(아이디,이름,이메일,핸드폰,성별,생년월일) 내역 불러옴
     - 아이디를 제외한 모든 정보 수정 가능
     - 수정 버튼 클릭 시 비밀번호 확인 페이지로 이동<br>
    
------------

3. <h3>회원 탈퇴</h3>

![회원탈퇴](https://github.com/seo02wow/Okitchen/assets/135966211/4e4554d6-9560-4378-b234-ded4a39927cd)



**회원 탈퇴 페이지**

  * 구현 기능 설명   
	   - 개인정보 수정 페이지에서 탈퇴 버튼 클릭 시 페이지 이동
	   - 현재 비밀번호 입력 시 탈퇴 처리 <br>

 ------------

 4. <h3>아이디 찾기, 비밀번호 재설정</h3>

![아이디찾기_비밀번호재설정](https://github.com/seo02wow/Okitchen/assets/135966211/2f0e75d6-3a72-4d47-ada9-b6822125026b)



**아이디 찾기 및 비밀번호 재설정 페이지**
  * 구현 기능 설명   
	   - 아이디 찾기 : 가입 시 입력한 이름 및 핸드폰 번호 입력
     - 비밀번호 재설정 : 아이디 및 핸드폰 번호를 통한 인증번호 확인 후 비밀번호 재설정
     - coolsms을 통한 인증번호 전송 후 인증<br>

 ------------

5. <h3>상품 검색</h3>

![상품검색](https://github.com/seo02wow/Okitchen/assets/135966211/69db9faa-d355-4ffd-8f42-c92206c2a977)



**상품 검색 페이지**

  * 구현 기능 설명   
	   - 검색어에 해당하는 상품명, 브랜드 통합 검색 
	   - 검색어에 해당하는 게시물 건수 조회
	   - 검색어 미입력시 검색 불가<br>
    
------------

6. <h3>상품 찜하기</h3>

![상품찜](https://github.com/seo02wow/Okitchen/assets/135966211/86e607c7-4724-4f07-ba16-9cefe0537a62)

  

**상품 찜하기 페이지**

  * 구현 기능 설명   
	   - 로그아웃 상태에서 찜 누를 경우 로그인 페이지로 이동
     - 상품 상세 페이지에서 흰색 하트 클릭 시 찜한 상품 추가
     - 찜한 상품의 경우 상품상세 페이지에서 주황색 하트로 표시
     - 마이페이지에서 찜한 상품 조회 및 삭제,장바구니 담기 가능 <br>  
    
------------

7. <h3>관리자(회원조회)</h3>

![회원조회](https://github.com/seo02wow/Okitchen/assets/135966211/106f77a4-88de-4f54-8797-8c0896d931ff)



**관리자 회원조회 페이지**

  * 구현 기능 설명   
	   - 모든 회원 조회 가능
	   - 비밀번호 제외한 정보 조회 가능 <br>
    
