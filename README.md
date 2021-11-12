# 📍 [Assignment 4] - 8퍼센트

<p align="center">

  <h2 align="center">🍴 Team 제6볶음 🍴</h2>
  <p align="center" width="50%">
  <img src="https://user-images.githubusercontent.com/73830753/141292063-a61a979d-4178-4e60-a472-df12c270bb80.jpg"/>
  <p align="center">
    각기 다른 재료가 모여 맛있는 제육볶음을 만들듯,<br> 
    서로 다른 개성있는 개인이 모여 멋진 결과물을 만들어내는 Team 제6볶음입니다. 
  </p>
  </p>

</p>

## 💁‍♀️ Members

| 이름   | github                                    | 담당 기능                |
| ------ | ----------------------------------------- | ------------------------ |
| 신재민 | [shinjam](https://github.com/shinjam)     | Test코드 적용, 배포      |
| 신우주 | [shinwooju](https://github.com/shinwooju) | 개인 사정으로 불참       |
| 최혜림 | [rimi0108](https://github.com/rimi0108)   | 거래 내역 조회 api       |
| 강성묵 | [miranaky](https://github.com/miranaky)   | 전체 총괄, 계좌 출금 api |
| 김민규 | [SkyStar-K](https://github.com/SkyStar-K) |                          |

## ⭐ 과제 출제 기업 정보

- 기업명 : 8퍼센트
- [8퍼센트 사이트](https://8percent.kr/)
- [wanted 채용공고 링크](https://www.wanted.co.kr/wd/64695)

## ⭐ 과제 내용

### **[필수 포함 사항]**

- READ.ME 작성
  - 프로젝트 빌드, 자세한 실행 방법 명시
  - 구현 방법과 이유에 대한 간략한 설명
  - 완료된 시스템이 배포된 서버의 주소
  - Swagger나 Postman을 통한 API 테스트할때 필요한 상세 방법
  - 해당 과제를 진행하면서 회고 내용 블로그 포스팅
- Swagger나 Postman을 이용하여 API 테스트 가능하도록 구현

<aside>
📝 “계좌 거래 API”를 구현해주세요. API는 3가지가 구현되어야 합니다.

</aside>

**✔️ API 목록**

---

- 거래내역 조회 API
- 입금 API
- 출금 API

**✔️ 주요 고려 사항은 다음과 같습니다.**

---

- 계좌의 잔액을 별도로 관리해야 하며, 계좌의 잔액과 거래내역의 잔액의 무결성의 보장
- DB를 설계 할때 각 칼럼의 타입과 제약

**✔️ 구현하지 않아도 되는 부분은 다음과 같습니다.**

---

- 문제와 관련되지 않은 부가적인 정보. 예를 들어 사용자 테이블의 이메일, 주소, 성별 등
- 프론트앤드 관련 부분

**✔️ 제약사항은 다음과 같습니다.**

---

- (**8퍼센트가 직접 로컬에서 실행하여 테스트를 원하는 경우를 위해**) 테스트의 편의성을 위해 mysql, postgresql 대신 sqllite를 사용해 주세요.

**✔️ 상세설명**

---

**1)** 거래내역 조회 **API**

- 아래와 같은 조회 화면에서 사용되는 API를 고려하시면 됩니다.
  [https://lh6.googleusercontent.com/PdtI4YvVu3biJ0TyEGCHVrR0fAPOQsILYHEczQHmR3UMKEINxlIjjp\_-3gOGu5yGh3YXpxbegNYqNCEosUosq3nKRTMpte6ZiRUccX8iRlD5rxLJ1HWFy6E2HcMFMIMGZO7eVQl5](https://lh6.googleusercontent.com/PdtI4YvVu3biJ0TyEGCHVrR0fAPOQsILYHEczQHmR3UMKEINxlIjjp_-3gOGu5yGh3YXpxbegNYqNCEosUosq3nKRTMpte6ZiRUccX8iRlD5rxLJ1HWFy6E2HcMFMIMGZO7eVQl5)

거래내역 API는 다음을 만족해야 합니다.

- 계좌의 소유주만 요청 할 수 있어야 합니다.
- 거래일시에 대한 필터링이 가능해야 합니다.
- 출금, 입금만 선택해서 필터링을 할 수 있어야 합니다.
- Pagination이 필요 합니다.
- 다음 사항이 응답에 포함되어야 합니다.
  - 거래일시
  - 거래금액
  - 잔액
  - 거래종류 (출금/입금)
  - 적요

**2)** 입금 **API**

입금 API는 다음을 만족해야 합니다.

- 계좌의 소유주만 요청 할 수 있어야 합니다.

**3)** 출금 **API**

출금 API는 다음을 만족해야 합니다.

- 계좌의 소유주만 요청 할 수 있어야 합니다.
- 계좌의 잔액내에서만 출금 할 수 있어야 합니다. 잔액을 넘어선 출금 요청에 대해서는 적절한 에러처리가 되어야 합니다.

**4)** 가산점

다음의 경우 가산점이 있습니다.

- Unit test의 구현
- Functional Test 의 구현 (입금, 조회, 출금에 대한 시나리오 테스트)
- 거래내역이 1억건을 넘어갈 때에 대한 고려
  - 이를 고려하여 어떤 설계를 추가하셨는지를 README에 남겨 주세요.

## 🛠 사용 기술 및 tools

> - Back-End : <img src="https://img.shields.io/badge/Python 3.8-3776AB?style=for-the-badge&logo=Python&logoColor=white"/>&nbsp;<img src="https://img.shields.io/badge/Django 3.2-092E20?style=for-the-badge&logo=Django&logoColor=white"/>&nbsp;<img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=SQLite&logoColor=white"/>
> - Deploy : <img src="https://img.shields.io/badge/AWS_EC2-232F3E?style=for-the-badge&logo=Amazon&logoColor=white"/>&nbsp;<img src="https://img.shields.io/badge/Docker-0052CC?style=for-the-badge&logo=Docker&logoColor=white"/>
> - ETC : <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white"/>&nbsp;<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"/>&nbsp;<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"/>

## 🏄‍♀️ 모델링

![modeling](https://user-images.githubusercontent.com/73830753/141414993-121661f4-4eda-4404-a4df-91a633270c09.png)

## 🖇 API

[Postman API Document](https://documenter.getpostman.com/view/13670333/UVC5F7t1)

## Coverage

```
$ pytest --cov
```

## 구현 기능

### 유저 회원가입 및 로그인

### 회원 별 계좌 생성

### 입금

### 출금

### 거래내역 조회

## 설치 및 실행 방법

</br>

### Local 개발 및 테스트용

```bash
    # git clone
    git clone https://github.com/JE6BOKM/wanted.git && cd wanted

    # 실행
    docker-compose -f docker/compose/local.yml up
```

### 배포용

```bash
    # 실행
    docker-compose -f docker/compose/prod.yml up
```

## 📁 폴더 구조

# Reference

이 프로젝트는 원티드x위코드 백엔드 프리온보딩 과제 일환으로 [8퍼센트](https://8percent.kr/)에서 출제한 과제를 기반으로 만들었습니다.
