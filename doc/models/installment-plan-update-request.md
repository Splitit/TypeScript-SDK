
# Installment Plan Update Request

## Structure

`InstallmentPlanUpdateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `trackingNumber` | `string \| undefined` | Optional | - |
| `capture` | `boolean \| undefined` | Optional | - |
| `shippingStatus` | [`ShippingStatusEnum \| undefined`](../../doc/models/shipping-status-enum.md) | Optional | - |
| `newAmount` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "RefOrderNumber": "RefOrderNumber2",
  "TrackingNumber": "TrackingNumber6",
  "Capture": false,
  "ShippingStatus": "Shipped",
  "NewAmount": "NewAmount4"
}
```

