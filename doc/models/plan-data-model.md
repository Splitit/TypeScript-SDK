
# Plan Data Model

## Structure

`PlanDataModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `totalAmount` | `string` | Required | - |
| `currency` | `string \| undefined` | Optional | - |
| `numberOfInstallments` | `number \| null \| undefined` | Optional | - |
| `terminalId` | `string \| undefined` | Optional | - |
| `purchaseMethod` | [`PurchaseMethodEnum`](../../doc/models/purchase-method-enum.md) | Required | - |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `extendedParams` | `Record<string, string> \| undefined` | Optional | - |
| `firstInstallmentAmount` | `string \| undefined` | Optional | - |
| `firstInstallmentDate` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "TotalAmount": "TotalAmount4",
  "Currency": "Currency6",
  "NumberOfInstallments": 154,
  "TerminalId": "TerminalId8",
  "PurchaseMethod": "ECommerce",
  "RefOrderNumber": "RefOrderNumber2",
  "ExtendedParams": {
    "key0": "ExtendedParams6",
    "key1": "ExtendedParams5",
    "key2": "ExtendedParams4"
  }
}
```

