---
description: 사용자 식별, 검색 수집
---

## 1. 일반

```
사용자 식별
검색
```


### 1.1. 사용자 식별

* 이벤트 명: **```UserInfo```**
* 데이터 포맷

```json
{
	"id": 1,
	"email": "test@gmail.com",
	"name": "tester",
	"age": 30,
	"birthday": "2000-01-01",
	"createdAt": "2021-06-17",
	"gender": "남",
	"phone": "01012341234",
	"website": "www.google.com"
}
```

|키값|설명|타입|
|------|---|---|
|id|회원을 구분하는 고유값|integer|
|email|회원 이메일|string|
|name|회원 이름|string|
|age|회원 나이|integer|
|birthday|회원 생일|string (yyyy-mm-dd)|
|createdAt|회원 등록일|string (yyyy-mm-dd)|
|gender|회원 성별|string(남 / 여)|
|phone|회원 연락처|string (ddddddddddd)|
|website|해당 사이트|string|



### 1.2. 검색

* 이벤트 명: **```Products Searched```**
* 데이터 포맷

```json
{
  "query": "검색어"
}
```

|키값|설명|타입|
|------|---|---|
|Query|검색 키워드|string|