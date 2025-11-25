
# Refund Model

## Structure

`RefundModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `refundId` | `string \| undefined` | Optional | - |
| `submitDate` | `string` | Required | - |
| `totalAmount` | `number` | Required | - |
| `status` | [`RefundStatusEnum`](../../doc/models/refund-status-enum.md) | Required | - |
| `nonCreditRefundAmount` | `number` | Required | - |
| `creditRefundAmount` | `number` | Required | - |
| `referenceId` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "RefundId": "RefundId0",
  "SubmitDate": "2016-03-13T12:52:32.123Z",
  "TotalAmount": 115.92,
  "Status": "Pending",
  "NonCreditRefundAmount": 172.08,
  "CreditRefundAmount": 159.38,
  "ReferenceId": "ReferenceId8"
}
```

