---
description: 제품 클릭, 조회, 리뷰, 관심 컨텐츠 등록, 관심 컨텐츠 제거, 북마크 페이지 접속
---

## 3. 제품

```
클릭
조회
리뷰
관심 컨텐츠 등록
관심 컨텐츠 제거
북마크 페이지 접속
```



### 3.1. 제품(컨텐츠) 클릭

* 이벤트 명:  **```Product Clicked```**
* 데이터 포맷

```json
{
    "product_id": "AS0812XA", 
    "sku": "0",												
    "category": "의류",
    "name": "의류1",
    "brand": "브랜드",
    "variant": "종류",
    "price": 12000,
    "quantity": 1,
    "coupon": 10000,
    "position": 1,
    "url": "http://test.com/product?productNo=AS0812XA",
    "image_url": "http://test.com/product/test.png"
}
```

|키값|설명|타입|
|------|---|---|
|product_id|상품 또는 콘텐츠 고유 아이디|string|
|sku|상품을 구분하는 구분값|string|
|category|상품 또는 콘텐츠 카테고리|string|
|name|상품 또는 콘텐츠 이름|string|
|brand|상품 또는 콘텐츠 브랜드|string|
|variant|상품 또는 콘텐츠 종류|string|
|price|상품 또는 콘텐츠 가격|integer|
|quantity|상품 또는 콘텐츠 수량|integer|
|coupon|쿠폰 적용 시|integer|
|position|해당 상품 또는 콘텐츠의 순서|integer|
|url|상품 또는 콘텐츠 URL|string|
|image_url|상품 또는 콘텐트 이미지 URL|string|



### 3.2. 제품(컨텐츠) 조회

*  이벤트 명: Product Viewed
* 데이터 포맷

```json
{
    "product_id": "AS0812XA",
    "sku": "0",
    "category": "의류",
    "name": "의류1",
    "brand": "브랜드",
    "variant": "종류",
    "price": 12000,
    "quantity": 1,
    "coupon": 10000,
    "currency": "krw",
    "position": 3,
    "value": 18.99,
    "url": "http://test.com/product?productNo=AS0812XA",
    "image_url": "http://test.com/product/test.png"
}
```

| 키값       | 설명                         | 타입    |
| ---------- | ---------------------------- | ------- |
| product_id | 상품 또는 콘텐츠 고유 아이디 | string  |
| sku        | 상품을 구분하는 구분값       | string  |
| category   | 상품 또는 콘텐츠 카테고리    | string  |
| name       | 상품 또는 콘텐츠 이름        | string  |
| brand      | 상품 또는 콘텐츠 브랜드      | string  |
| variant    | 상품 또는 콘텐츠 종류        | string  |
| price      | 상품 또는 콘텐츠 가격        | integer |
| quantity   | 상품 또는 콘텐츠 수량        | integer |
| coupon     | 쿠폰 적용 시                 | integer |
| currency   | 화폐 구분                 | string (KRW, USDT) |
| position   | 해당 상품 또는 콘텐츠의 순서 | integer |
| url        | 상품 또는 콘텐츠 URL         | string  |
| image_url  | 상품 또는 콘텐트 이미지 URL  | string  |



### 3.3. 제품 리뷰

* 이벤트 명: **``` Product Reviewed```**
* 데이터 포맷

```json
{
    "product_id": "AS0812XA",
    "review_id": "RD00001",
    "review_body": "",
    "rating": 5
}
```

| 키값        | 설명                         | 타입            |
| ----------- | ---------------------------- | --------------- |
| product_id  | 상품 또는 콘텐츠 고유 아이디 | string          |
| review_id   | 리뷰 고유값                  | string          |
| review_body | 상품 또는 콘텐츠 리뷰 내용   | string          |
| rating      | 상품 또는 콘텐츠 별점        | double(max: 10) |



### 3.4. 관심 컨텐츠 등록

* 이벤트 명: **```Product Added```**
* 데이터 포맷

```json
{
  	"product_id": "AS0812XA"
}
```

| 키값       | 설명                         | 타입   |
| ---------- | ---------------------------- | ------ |
| product_id | 상품 또는 콘텐츠 고유 아이디 | string |



### 3.5. 관심 컨텐츠 제거

* 이벤트 명: **```Product Removed```**
* 데이터 포맷

```json
{
  	"product_id": "AS0812XA"
}
```

| 키값       | 설명                         | 타입   |
| ---------- | ---------------------------- | ------ |
| product_id | 상품 또는 콘텐츠 고유 아이디 | string |



### 3.6. 북마크 페이지 이동

* 이벤트 명: **```Cart Viewed```**
* 데이터 포맷

```json
{
  "products": [{
    "product_id": "AS0812XA",
    "name": "의류 1",
    "price": 12000,
    "prositon": 3,
    "category": "의류"
  }]
}
```

| 키값     | 설명                      | 타입      |
| -------- | ------------------------- | --------- |
| Products | 북마크 된 제품(컨텐츠) 들 | Product[] |

* Product Type

| 키값       | 설명                         | 타입    |
| ---------- | ---------------------------- | ------- |
| product_id | 상품 또는 콘텐츠 고유 아이디 | string  |
| name       | 상품 또는 콘텐츠 이름        | string  |
| price      | 상품 또는 콘텐츠 가격        | integer |
| prositon   | 해당 상품 또는 콘텐츠의 순서 | integer |
| category   | 상품 또는 콘텐츠 카테고리    | string  |



