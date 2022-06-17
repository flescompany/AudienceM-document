# 2. identify user

```
analytics.identify(userId, traits)
```

* example

```
analytics.identify('12312312', {
	"birthday": "2000",
	"gender": "1",
})
```



| FIELD  | TYPE   | DESCRIPTION                                     |
| ------ | ------ | ----------------------------------------------- |
| userId | string | The database ID for user. must be unique.       |
| traits | Object | A dictionary of traits you know about the user. |

* traits

```jsdoc
{
	"birthday": "2000",
	"gender": "1",
}
```

| key      | value | type               |
| -------- | ----- | ------------------ |
| birthday | 회원 생일 | string (yyyy)      |
| gender   | 회원 성별 | string (남:1 / 여:2) |
