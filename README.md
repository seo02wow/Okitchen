# Spring-Project-Okitchen
스프링 + JSP 식품 판매 사이트

------------

# 📝개요

* 프로젝트 명 : Okitchen

* 일정 : 2023년 11월 07일 ~ 2023년 11월 29일

* 개발 목적 : 식품 쇼핑몰 밀 판매자가 상품을 등록, 관리자가 누적된 데이터를 활용할 수 있는 사이트 제작

* 개발 환경
  - Server : Apache-tomcat-8.5.61
  - IDE : STS 3.9
  - Database : Oracle SQL Developer ( version 18.3.0 )
  - Programming Language : JAVA, HTML, CSS, JavaScript, JSP, SQL
  - Framework/flatform : Spring, mybatis, jQuery 3.7.1, Bootstrap v5.3.1x
  - API : Kakao map, summernote


------------

# 📝내용

* 팀원별 역할
  - 공통 : 기획, 요구 사항 정의, DB 설계, 화면 구현
  - 김서영 : 일반 회원 CRUD, 로그인, 상품 검색, 찜하기 
  - 박수진 : 판매자 회원 CRUD, 로그인, 관리자 기능(상품 관리)
  - 신민기 : 커뮤니티 게시판 CRUD, 관리자 (매출 조회,배송 상태 변경)
  - 이주녕 : 장바구니 CRUD, 결제하기, 
  - 이초희 : 상품 CRUD, 상품 카테고리 및 상세 조회
  - 전의진 : 상품문의 CRUD , 상품후기 CRUD 

* 구현 기능
  - 회원가입
  - 로그인, 로그아웃
  - 상품 검색
  - 찜하기

* DB 설계<br>
![image](https://github.com/seo02wow/Okitchen/assets/135966211/77e5f81d-5b27-4bfa-be1a-107c94053aa1)


------------

# 📝구현 기능

## 회원가입

 1. <h3 id="notice">회원가입</h3>

![회원가입](https://github.com/seo02wow/Okitchen/assets/135966211/6d9a03e7-867e-4717-81fb-bad66a0cc229)

  **회원가입 페이지**
   
  * 구현 기능 설명
    - 아이디 : 7자 이상 16자 이하 입력 , 중복 체크
    - 비밀번호 : 10자 이상 16자리 이하 입력
    - 이메일 : 중복 체크 
    - 주소 : 카카오 주소 API를 이용한 주소 검색 
    - 핸드폰 : 핸드폰 인증 번호 API를 이용한 인증번호 전송 
    - 생년월일 : 만 14세 이상만 가입 가능
    - DB값 검증
    - 로그인 시 세션(Session) 생성


------------

2. <h3>개인정보 수정</h3>
