
# Authorization Model

## Structure

`AuthorizationModel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`GwAuthorizationStatusEnum`](../../doc/models/gw-authorization-status-enum.md) | Required | - |
| `date` | `string \| undefined` | Optional | - |
| `splititErrorResultCode` | `string \| undefined` | Optional | - |
| `gatewayTransactionID` | `string \| undefined` | Optional | - |
| `gatewayResultCode` | `string \| undefined` | Optional | - |
| `gatewayResultMessage` | `string \| undefined` | Optional | - |
| `threeDSRedirect` | [`ThreeDsRedirectDataV3 \| undefined`](../../doc/models/three-ds-redirect-data-v3.md) | Optional | - |
| `cAVV` | `string \| undefined` | Optional | - |
| `eCI` | `string \| undefined` | Optional | - |
| `gatewaySourceResponse` | `string \| undefined` | Optional | - |

## Example (as JSON)

```json
{
  "Status": "Canceled",
  "Date": "2016-03-13T12:52:32.123Z",
  "SplititErrorResultCode": "SplititErrorResultCode6",
  "GatewayTransactionID": "GatewayTransactionID0",
  "GatewayResultCode": "GatewayResultCode2",
  "GatewayResultMessage": "GatewayResultMessage8"
}
```

