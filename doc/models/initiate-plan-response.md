
# Initiate Plan Response

## Structure

`InitiatePlanResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string \| undefined` | Optional | - |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `purchaseMethod` | [`PurchaseMethodEnum \| undefined`](../../doc/models/purchase-method-enum.md) | Optional | - |
| `status` | [`PlanStatusEnum`](../../doc/models/plan-status-enum.md) | Required | - |
| `currency` | `string \| undefined` | Optional | - |
| `amount` | `number \| undefined` | Optional | - |
| `extendedParams` | `Record<string, string> \| undefined` | Optional | - |
| `shopper` | [`ShopperData \| undefined`](../../doc/models/shopper-data.md) | Optional | - |
| `billingAddress` | [`AddressData \| undefined`](../../doc/models/address-data.md) | Optional | - |
| `checkoutUrl` | `string \| undefined` | Optional | - |
| `principalAmount` | `number \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "InstallmentPlanNumber": "InstallmentPlanNumber6",
  "RefOrderNumber": "RefOrderNumber6",
  "PurchaseMethod": "InStore",
  "Status": "Initialized",
  "Currency": "Currency0",
  "Amount": 69.84
}
```

