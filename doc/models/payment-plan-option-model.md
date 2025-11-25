
# Payment Plan Option Model

## Structure

`PaymentPlanOptionModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `numberOfInstallments` | `number` | Required | - |
| `firstInstallmentAmount` | `number` | Required | - |
| `installmentAmount` | `number` | Required | - |
| `lastInstallmentAmount` | `number` | Required | - |
| `links` | [`LinksModel \| undefined`](../../doc/models/links-model.md) | Optional | - |
| `termsAndConditionsBrief` | `string \| undefined` | Optional | - |
| `installmentFrequency` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "NumberOfInstallments": 148,
  "FirstInstallmentAmount": 45.62,
  "InstallmentAmount": 232.3,
  "LastInstallmentAmount": 187.9,
  "Links": null,
  "TermsAndConditionsBrief": "TermsAndConditionsBrief6",
  "InstallmentFrequency": "InstallmentFrequency2"
}
```

