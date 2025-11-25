
# Installment Plan Get Response

## Structure

`InstallmentPlanGetResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string \| undefined` | Optional | - |
| `dateCreated` | `string` | Required | - |
| `refOrderNumber` | `string \| undefined` | Optional | - |
| `purchaseMethod` | [`PurchaseMethodEnum \| undefined`](../../doc/models/purchase-method-enum.md) | Optional | - |
| `status` | [`PlanStatusEnum`](../../doc/models/plan-status-enum.md) | Required | - |
| `currency` | `string \| undefined` | Optional | - |
| `originalAmount` | `number \| undefined` | Optional | - |
| `amount` | `number \| undefined` | Optional | - |
| `authorization` | [`AuthorizationModel \| undefined`](../../doc/models/authorization-model.md) | Optional | - |
| `shopper` | [`ShopperData \| undefined`](../../doc/models/shopper-data.md) | Optional | - |
| `billingAddress` | [`AddressData \| undefined`](../../doc/models/address-data.md) | Optional | - |
| `paymentMethod` | [`PaymentMethodModel \| undefined`](../../doc/models/payment-method-model.md) | Optional | - |
| `extendedParams` | `Record<string, string> \| undefined` | Optional | - |
| `installments` | [`Installment[] \| undefined`](../../doc/models/installment.md) | Optional | - |
| `refunds` | [`RefundModel[] \| undefined`](../../doc/models/refund-model.md) | Optional | - |
| `links` | [`LinksData \| undefined`](../../doc/models/links-data.md) | Optional | - |

## Example (as JSON)

```json
{
  "InstallmentPlanNumber": "InstallmentPlanNumber4",
  "DateCreated": "2016-03-13T12:52:32.123Z",
  "RefOrderNumber": "RefOrderNumber4",
  "PurchaseMethod": "InStore",
  "Status": "Cleared",
  "Currency": "Currency8",
  "OriginalAmount": 2.6
}
```

