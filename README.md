# otpbuddy.xyz-api



## API GETAWAY

#### Get Available Balance

```http
  GET /v1/api/getBalance?token=<token>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |

###### Response
```javascript
{
  status:200,
  data : {
    balance : 500
  }
}
```


#### Get New Number

```http
  GET /v1/api/getNumber?token=<token>&sever=in&product_id=<product_id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `server` | `string` | **Required**. Server 2 digits name , eg IN|
| `product_id` | `string` | **Required**. Product id |

###### Response
```javascript
{
  status:200,
  data : {
    balance : 500
  }
}
``` 

#### Get OTP of Number

```http
  GET /v1/api/getSms?token=<token>&id=<number_id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |

###### Response
```javascript
{
  status:200,
  data : {
    balance : 500
  }
}
``` 


#### Set Status

```http
  GET /v1/api/setStatus?token=<token>&id=<number_id>&status=<status_code>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |
| `status_code` | `number` | **Required**. status_code = 8 -> Cancel Number  |

###### Response
```javascript
{
  status:200,
  data : {
    balance : 500
  }
}
``` 

#### Get Status

```http
  GET /v1/api/getStatus?token=<token>&id=<number_id>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |


###### Response
```
{
  status:200,
  data : {
    balance : 500
  }
}
``` 


#### Get Products

```http
  GET /v1/api/getStatus?token=<token>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your API key |
| `id` | `string` | **Required**. ID of Number |


###### Response
```json
{
  status:200,
  data : {
   whatsapp :{
     id:...,
     price:..,
   },
   .....
  }
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




