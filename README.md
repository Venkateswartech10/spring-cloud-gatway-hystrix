# spring-cloud-gateway-hystrix

<img width="940" height="599" alt="image" src="https://github.com/user-attachments/assets/10697808-2dde-4e34-b6a7-55c0900b474e" />

<img width="940" height="628" alt="image" src="https://github.com/user-attachments/assets/8895c2f0-2a8e-40b1-a49f-bc6ba114445e" />

<img width="940" height="576" alt="image" src="https://github.com/user-attachments/assets/9c9f951f-5110-49b9-9b4a-01b49861882d" />





API-GateWay
-----------
```bash
URL : http://localhost:8989/order/bookOrder
HTTP Method : POST
```
Json Request :
```json
{
	"order":{
		"id":103,
		"name":"Mobile",
		"qty":1,
		"price":8000
		
	},
	"payment":{}
}
```
Json Response :
```json
{
    "order": {
        "id": 26,
        "name": "ear-phone",
        "qty": 5,
        "price": 4000
    },
    "amount": 4000,
    "transactionId": "9a021fa6-2061-4332-bdb7-b1358b3430c2",
    "message": "payment processing successful and order placed"
}

```
```bash
URL : http://localhost:8989/payment/26
HTTP Method : GET
```
Json Response :
```json
{
    "paymentId": 1,
    "transactionId": "d86cfeca-0b26-455e-a1a2-ac3e53707829",
    "orderId": 103,
    "paymentStatus": "SUCCESS",
    "amount":4000
}
```
