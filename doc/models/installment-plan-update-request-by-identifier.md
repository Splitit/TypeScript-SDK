
# Installment Plan Update Request by Identifier

## Structure

`InstallmentPlanUpdateRequestByIdentifier`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `trackingNumber` | `string \| undefined` | Optional | - |
| `capture` | `boolean \| undefined` | Optional | - |
| `shippingStatus` | [`ShippingStatusEnum \| undefined`](../../doc/models/shipping-status-enum.md) | Optional | - |
| `newAmount` | `number \| undefined` | Optional | - |
| `identifier` | [`IdentifierContract \| undefined`](../../doc/models/identifier-contract.md) | Optional | - |

## Example (as JSON)

```json
{
  "RefOrderNumber": "RefOrderNumber2",
  "TrackingNumber": "TrackingNumber6",
  "Capture": false,
  "ShippingStatus": "Pending",
  "NewAmount": 233.74
}
```

