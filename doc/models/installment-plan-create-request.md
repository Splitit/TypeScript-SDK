
# Installment Plan Create Request

## Structure

`InstallmentPlanCreateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoCapture` | `boolean` | Required | - |
| `attempt3dSecure` | `boolean \| undefined` | Optional | - |
| `termsAndConditionsAccepted` | `boolean` | Required | - |
| `shopper` | [`ShopperData \| undefined`](../../doc/models/shopper-data.md) | Optional | - |
| `planData` | [`PlanDataModel \| undefined`](../../doc/models/plan-data-model.md) | Optional | - |
| `billingAddress` | [`AddressDataModel \| undefined`](../../doc/models/address-data-model.md) | Optional | - |
| `paymentMethod` | [`PaymentMethodModel \| undefined`](../../doc/models/payment-method-model.md) | Optional | - |
| `redirectUrls` | [`RedirectionEndpointsModel \| undefined`](../../doc/models/redirection-endpoints-model.md) | Optional | - |
| `processingData` | [`ProcessingData \| undefined`](../../doc/models/processing-data.md) | Optional | - |
| `eventsEndpoints` | [`EventsEndpointsModel \| undefined`](../../doc/models/events-endpoints-model.md) | Optional | - |

## Example (as JSON)

```json
{
  "AutoCapture": false,
  "Attempt3dSecure": false,
  "TermsAndConditionsAccepted": false,
  "Shopper": null,
  "PlanData": null,
  "BillingAddress": null,
  "PaymentMethod": null
}
```

