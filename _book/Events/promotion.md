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
|promotion_id|프로모션 코드||
|creative|프로모션 배치 영역||
|name|프로모션 제목||
|position|프로모션 배너 위치||



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
|promotion_id|프로모션 코드||
|creative|프로모션 배치 영역||
|name|프로모션 제목||
|position|프로모션 배너 위치||


