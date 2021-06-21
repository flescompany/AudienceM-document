---
description: 주문시작, 주문완료 수집
---

## 4. 주문

```
주문시작
주문완료
```



### 4.1. 주문시작

* 이벤트 명: **```Checkout Started```**
* 데이터 포맷

```json
{
	"order_id": "OR000001",	
	"affiliation": "제휴사",
	"value": 12000,			
	"revenue": 10000,		
	"shipping": 2000,		
	"tax": 0,						
	"discount": 0,			
	"coupon": 0,				
	"currency": "KRW",
	"products": [{
    "product_id": "AS0812XA",
    "sku": "0",
    "name": "의류1",
    "price": 12000,
    "quantity": 1,
    "category": "의류"
	}]
}
```

| 키값        | 설명        | 타입               |
| ----------- | ----------- | ------------------ |
| order_id    | 주문번호    | string             |
| affiliation | 제휴사      | string             |
| value       | 총 주문금액 | integer            |
| revenue     | 수익        | integer            |
| shipping    | 배송료      | integer            |
| tax         | 세금        | integer            |
| discount    | 할인        | integer            |
| coupon      | 사용한 쿠폰  | string             |
| currency    | 화폐구분    | string (KRW, USD) |
| products    | 주문제품    | Product[]          |

* Product Type

| 키값       | 설명                         | 타입    |
| ---------- | ---------------------------- | ------- |
| product_id | 상품 또는 콘텐츠 고유 아이디 | string  |
| sku        | 상품을 구분하는 구분값       | string  |
| name       | 상품 또는 콘텐츠 이름        | string |
| price      | 상품 또는 콘텐츠 가격        | integer |
| quantity   | 상품 또는 콘텐츠 수량        | integer |
| category   | 상품 또는 콘텐츠 카테고리    | string  |




### 4.2. 주문완료

* 이벤트 명: **```Order Completed```**
* 데이터 포맷

```json
{
  "transaction_id": "TX0000001",
  "value": 12000,
  "currency": "KRW",
  "tax": 0,
  "shipping": 0,
  "items": [{
    "id": "AS0812XA",
    "name": "의류1",
    "quantity": 1,
    "price": 12000
  }]
}
```

| 키값           | 설명 | 타입 |
| -------------- | ---- | ---- |
| transaction_id | 주문번호 | string |
| value          | 총 주문금액 | integer |
| currency       | 화폐구분 | string (KRW, USD) |
| tax            | 세금 | integer |
| shipping       | 배송료 | integer |
| items       | 주문제품 | Item |

* Item Type

| 키값           | 설명 | 타입 |
| -------------- | ---- | ---- |
| id | 상품 또는 콘텐츠 고유 아이디 | string |
| name       | 상품 또는 콘텐츠 이름 | string |
| quantity | 상품 또는 콘텐츠 수량 | integer |
| price       | 상품 또는 콘텐츠 가격 | integer |

