# QuickReply_Assignment_FDE
# QuickReply FDE Assignment

## Objective

Create an automation that:

1. Receives a Shopify order webhook
2. Checks if Order Tag contains "MakeOrder"
3. Checks if Customer Tag contains "ColdCustomer"
4. Checks if Order Amount is greater than ₹2500

If all conditions are met:

* Send onboarding email immediately
* Wait 5 minutes
* Send discount email

## Workflow

HTTP Trigger
→ Filter: Order Tag = MakeOrder
→ Filter: Customer Tag = ColdCustomer
→ Filter: Order Amount > 2500
→ Gmail: Welcome Email
→ Delay: 5 Minutes
→ Gmail: Discount Email

## Sample Payload

```json
{
  "id": 10001,
  "name": "#1001",
  "tags": "MakeOrder, Priority",
  "total_price": 3000,
  "currency": "INR",
  "customer": {
    "id": 5001,
    "first_name": "Rahul",
    "last_name": "Sharma",
    "email": "harshitgoyal2003@gmail.com",
    "tags": "ColdCustomer"
  }
}
```

## Testing

The workflow was tested using sample Shopify webhook payloads in Pipedream.

<img width="1918" height="1062" alt="image" src="https://github.com/user-attachments/assets/2854a7ef-4bdd-4e20-af0d-e487d733dd36" />

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/9867fe18-3137-4df2-a5a8-fb38bcc4bf58" />

<img width="1043" height="508" alt="image" src="https://github.com/user-attachments/assets/582b12b2-b53b-44bd-9c4a-3c5a97f7acf6" />

<img width="1005" height="478" alt="image" src="https://github.com/user-attachments/assets/0fdf6930-db1f-430e-b32c-acbb3945e8fc" />
<img width="1038" height="568" alt="image" src="https://github.com/user-attachments/assets/3f0a5c7a-40f8-4707-933e-41f265179a6d" />

<img width="1541" height="305" alt="image" src="https://github.com/user-attachments/assets/b748d877-681f-4939-98b5-f4f557ce3cbd" />



## Author

Nilesh Pandey
