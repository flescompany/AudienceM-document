# track event

```
analytics.track('event name',{properties})
```

| FIELD      | TYPE   | DESCRIPTION                               |
| ---------- | ------ | ----------------------------------------- |
| event name | string | The name of the event you’re tracking.    |
| properties | Object | A dictionary of properties for the event. |

## Order Complete

```
analytics.track('order_completed',{properties})
```

* example

```
analytics.track('order_completed',{
    idx:130324958
    value:10000,
    product_name: 'bicycle',
    product_id:'12345'
})
```

* event name: **`Order_Completed`**
* properties

```json
  {
    idx:130324958
    value:10000,
    product_name: 'bicycle',
    product_id:'12345'
}
```

| 키값            | 설명                | 타입      |
| ------------- | ----------------- | ------- |
| idx           | 주문번호              | string  |
| value         | 총 주문금액            | integer |
| product\_id   | unique product id | string  |
| product\_name | 주문제품              | string  |

## Product Click

```
analytics.track('order_clicked',{properties})
```

* example

```
analytics.track('product_clicked',{
    product_name: 'bicycle',
    product_id:'12345'
})
```

* event name: **`Product_Clicked`**
* properties

```json
{
   product_name: 'bicycle',
   product_id:'12345'
 }
```

| 키값            | 설명                | 타입     |
| ------------- | ----------------- | ------ |
| product\_id   | unique product id | string |
| product\_name | 주문제품              | string |