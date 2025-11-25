
# Installment

## Structure

`Installment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentNumber` | `number` | Required | - |
| `amount` | `number` | Required | - |
| `processDateTime` | `string \| undefined` | Optional | - |
| `status` | [`InstallmentStatusEnum`](../../doc/models/installment-status-enum.md) | Required | - |

## Example (as JSON)

```json
{
  "InstallmentNumber": 244,
  "Amount": 181.38,
  "ProcessDateTime": "2016-03-13T12:52:32.123Z",
  "Status": "Processed"
}
```

