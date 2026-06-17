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

## Author

Nilesh Pandey
