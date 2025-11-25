
# Installment Plan Refund Request

## Structure

`InstallmentPlanRefundRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string` | Required | - |
| `refundStrategy` | [`RefundStrategyEnum \| undefined`](../../doc/models/refund-strategy-enum.md) | Optional | - |
| `referenceId` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "Amount": "Amount4",
  "RefundStrategy": "FutureInstallmentsNotAllowed",
  "ReferenceId": "ReferenceId0"
}
```

