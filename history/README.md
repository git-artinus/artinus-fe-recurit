# ARTINUS Frontend Developer 과제

---
## 과제 내용
- [https://dummyjson.com/products](https://dummyjson.com/docs/products) API를 연동하여, 상품 목록 페이지와 상품 상세 페이지로 구성된 웹 페이지를 개발해 주세요.
- DummyJson Products API 는 실제 상점에서 판매되는 것처럼 구성된 가상의 상품 데이터를 JSON 형식으로 제공하는 무료 API입니다. 인증 없이 누구나 사용할 수 있으며, 페이징(limit, skip) 기능과 상세 검색 API를 지원합니다.

---

## 요구사항
### 리스트 페이지
- 응답 데이터를 테이블/카드/리스트 형태 등으로 페이지 구성
- 호출 예시
``` 
GET https://dummyjson.com/products?skip=0&limit=20
```
- 응답 예시
``` json
{
  "products": [
    {
      "id": 1,
      "title": "iPhone 9",
      "description": "An apple mobile which is nothing like apple",
      "price": 549,
      "discountPercentage": 12.96,
      "rating": 4.69,
      "stock": 94,
      "brand": "Apple",
      "category": "smartphones",
      "thumbnail": "https://cdn.dummyjson.com/product-images/1/thumbnail.jpg"
    },
    ...
  ],
  "total": 100,
  "skip": 0,
  "limit": 20
}
```
- 각 상품 정보에는 `thumbnail`, `title`, `price` 를 포함합니다.
- 20개씩 불러오며, 스크롤 기반 Lazy Load 기능을 포함합니다.


### 상세 페이지
- 리스트 페이지의 상품 항목 클릭 시, 해당 상품의 상세 페이지로 이동
- 호출 예시
``` 
GET https://dummyjson.com/products/{id}
```
- 응답 예시
``` json
{
  "id": 1,
  "title": "Essence Mascara Lash Princess",
  "price": 9.99,
  "tags": [
    "beauty",
    "face powder"
  ],  
  "thumbnail": "https://cdn.dummyjson.com/product-images/beauty/essence-mascara-lash-princess/thumbnail.webp"
  ...
}
```
- 상품 상세 정보에는 `thumbnail`, `title`, `price`, `tags` 를 포함합니다.


### 공통
- 데이터 로딩 중에는 로딩 스피너 또는 텍스트 형태의 UI 요소를 표시해야 합니다.
- 빌드 시, 파일 크기 최소화와 캐싱 최적화가 포함되어야 합니다.
- 구현한 결과물은 정적 사이트로 배포합니다.
- 요구사항에 명시되지 않은 부분은 자유롭게 구현해 주세요.

---

## 제약 사항
- Frontend Framework 사용 자유
- 디자인 자유 (단, 최소한의 사용자 중심 UI/UX 고려)
- 외부 라이브러리 사용 자유

---

## 제출 방법
- 분석 및 구현 내용을 `readme.md` 파일에 정리해 주세요.
  - 포함 내용:
    - 개발 환경
    - 개발 내용
    - 빌드 및 실행 방법
    - 배포한 정적 사이트 URL 
- Github Repository URL 제출

---

## 평가 항목
- 프로젝트 구성
- 요구사항 이해
- 기능 구현 정확도
- 코드 구조 및 명료성
- 기술 선택 및 설명 문서
