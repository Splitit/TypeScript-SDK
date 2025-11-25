
# Installment Plan Update Response

## Structure

`InstallmentPlanUpdateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `installmentPlanNumber` | `string \| undefined` | Optional | - |
| `status` | [`PlanStatusEnum`](../../doc/models/plan-status-enum.md) | Required | - |
| `shippingStatus` | [`ShippingStatusEnum`](../../doc/models/shipping-status-enum.md) | Required | - |
| `newAmount` | `number \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "RefOrderNumber": "RefOrderNumber2",
  "InstallmentPlanNumber": "InstallmentPlanNumber2",
  "Status": "PendingCapture",
  "ShippingStatus": "Delivered",
  "NewAmount": 233.54
}
```

