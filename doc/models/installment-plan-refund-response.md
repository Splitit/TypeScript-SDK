
# Installment Plan Refund Response

## Structure

`InstallmentPlanRefundResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refundId` | `string \| undefined` | Optional | - |
| `installmentPlanNumber` | `string \| undefined` | Optional | - |
| `currency` | `string \| undefined` | Optional | - |
| `nonCreditRefundAmount` | `number \| undefined` | Optional | - |
| `creditRefundAmount` | `number \| undefined` | Optional | - |
| `summary` | [`RefundSummary \| undefined`](../../doc/models/refund-summary.md) | Optional | - |
| `referenceId` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "RefundId": "RefundId8",
  "InstallmentPlanNumber": "InstallmentPlanNumber6",
  "Currency": "Currency0",
  "NonCreditRefundAmount": 1.76,
  "CreditRefundAmount": 182.3
}
```

