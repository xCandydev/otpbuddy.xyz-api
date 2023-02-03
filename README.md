# otpbuddy.xyz-api



## API GETAWAY

#### Get Available Balance

```
  GET https://otpbuddy.xyz/v1/api/getBalance?token=<token>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |

###### Response
```javascript
{
  "status": 200,
  "data": {
        "balance": 42
    }
}
```


#### Buy Phone Number

```
  GET https://otpbuddy.xyz/v1/api/getNumber?token=<token>&server=in&product_id=<product_id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `server` | `string` | **Required**. Server 2 digits name , eg IN|
| `product_id` | `string` | **Required**. Product id |

###### Response
```javascript
{
  "status": 200,
  "data": {
    "number": "9163001XXXXX",
    "id": "63dca665627XXXXXX"
     }
}
``` 

#### Get SMS 

```
  GET https://otpbuddy.xyz/v1/api/getSms?token=<token>&id=<id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |

###### Response
```javascript
{
    "status": 200,
    "message": "Your Code is ######"
}
``` 


#### Cancel Number 

```
  GET https://otpbuddy.xyz/v1/api/cancelNumber?token=<token>&id=<id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |
| `status_code` | `number` | **Required**. status_code = 8 -> Cancel Number  |

###### Response
```javascript
{
    "status": 200,
    "message": "Cancelled"
}
``` 

#### Get Products

```
  GET https://otpbuddy.xyz/v1/api/getProducts?token=<token>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |


###### Response
```javascrit
{
    "status": 200,
    "data": [
    {
      "product_name": "Вконтакте",
      "price": 9,
      "product_id": "vk"
    },
    {..},
    {..},
    {..}
    ]
}
``` 


#### Country  CODES

| Country | CODE     | 
| :-------- | :------- |
| `INDIA` | `in` |  



#### STATUS CODES

| CODE | type     | Description                |
| :-------- | :------- | :------------------------- |
| `200` | `success` |  Action was success |
| `210` | `success` |  waiting for message |
| `201` | `error` | Invaild ID |
| `202` | `error` | Insufficient Balance |
| `203` | `error` | Product Not Found |
| `204` | `error` | Number Expires |
| `205` | `error` | Server ERROR |
| `206` | `error` | Invaild Parameter |




