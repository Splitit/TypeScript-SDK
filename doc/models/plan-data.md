
# Plan Data

## Structure

`PlanData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `terminalId` | `string \| undefined` | Optional | - |
| `totalAmount` | `string` | Required | - |
| `firstInstallmentAmount` | `number \| undefined` | Optional | - |
| `currency` | `string \| undefined` | Optional | - |
| `numberOfInstallments` | `number` | Required | - |
| `purchaseMethod` | [`PurchaseMethodEnum`](../../doc/models/purchase-method-enum.md) | Required | - |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `allowedInstallmentOptions` | `number[] \| undefined` | Optional | - |
| `tags` | `Record<string, string> \| undefined` | Optional | - |
| `processingData` | [`ProcessingData \| undefined`](../../doc/models/processing-data.md) | Optional | - |
| `firstInstallmentDate` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "TerminalId": "TerminalId8",
  "TotalAmount": "TotalAmount4",
  "FirstInstallmentAmount": 11.28,
  "Currency": "Currency6",
  "NumberOfInstallments": 2,
  "PurchaseMethod": "PhoneOrder",
  "RefOrderNumber": "RefOrderNumber2",
  "AllowedInstallmentOptions": [
    46,
    47
  ]
}
```

