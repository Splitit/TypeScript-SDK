
# Payment Method Model

## Structure

`PaymentMethodModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`PaymentMethodTypeEnum`](../../doc/models/payment-method-type-enum.md) | Required | - |
| `card` | [`CardData \| undefined`](../../doc/models/card-data.md) | Optional | - |
| `token` | `string \| undefined` | Optional | - |
| `bluesnapVaultedShopperToken` | [`BluesnapVaultedShopperToken \| undefined`](../../doc/models/bluesnap-vaulted-shopper-token.md) | Optional | - |
| `mockerShopperToken` | [`MockerShopperToken \| undefined`](../../doc/models/mocker-shopper-token.md) | Optional | - |
| `spreedlyToken` | [`SpreedlyToken \| undefined`](../../doc/models/spreedly-token.md) | Optional | - |
| `cardPAR` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "Type": "Card",
  "Card": null,
  "Token": "Token6",
  "BluesnapVaultedShopperToken": null,
  "MockerShopperToken": null,
  "SpreedlyToken": null
}
```

