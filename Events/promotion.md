---
description: 프로모션 조회, 프로모션 클릭
---

## 2. 프로모션 

```
조회
페이지 클릭
```



### 2.1. 프로모션 조회

* 이벤트 명: **```Promotion Viwed```**
* 데이터 포맷

```json
{
		"promotion_id": 0,
		"creative": "",	
		"name": "",
		"position": ""
}
```

|키값|설명|타입|
|------|---|---|
|promotion_id|프로모션 식별하는 고유값|string|
|creative|프로모션 배너의 위치식별자(top_banner_1)|string|
|name|프로모션 제목|string|



### 2.2. 프로모션 페이지 클릭

* 이벤트 명: **```Promotion Clicked```**
* 데이터 포맷

```json
{
		"promotion_id": 0,
		"creative": "",	
		"name": "",
		"position": ""
}
```

|키값|설명|타입|
|------|---|---|
|promotion_id|프로모션 식별하는 고유값|string|
|프로모션 배너의 위치식별자(top_banner_1)|string|
|name|프로모션 제목|string|


