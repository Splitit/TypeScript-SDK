
# Installment Plan Initiate Request

## Structure

`InstallmentPlanInitiateRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoCapture` | `boolean \| undefined` | Optional | - |
| `attempt3dSecure` | `boolean \| undefined` | Optional | - |
| `shopper` | [`ShopperData \| undefined`](../../doc/models/shopper-data.md) | Optional | - |
| `planData` | [`PlanDataModel \| undefined`](../../doc/models/plan-data-model.md) | Optional | - |
| `billingAddress` | [`AddressDataModel \| undefined`](../../doc/models/address-data-model.md) | Optional | - |
| `redirectUrls` | [`InitiateRedirectionEndpointsModel \| undefined`](../../doc/models/initiate-redirection-endpoints-model.md) | Optional | - |
| `uxSettings` | [`UxSettingsModel \| undefined`](../../doc/models/ux-settings-model.md) | Optional | - |
| `eventsEndpoints` | [`EventsEndpointsModel \| undefined`](../../doc/models/events-endpoints-model.md) | Optional | - |
| `processingData` | [`ProcessingData \| undefined`](../../doc/models/processing-data.md) | Optional | - |

## Example (as JSON)

```json
{
  "AutoCapture": false,
  "Attempt3dSecure": false,
  "Shopper": null,
  "PlanData": null,
  "BillingAddress": null
}
```

