
# Verify Authorization Response

## Structure

`VerifyAuthorizationResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isAuthorized` | `boolean` | Required | - |
| `authorizationAmount` | `number \| undefined` | Optional | - |
| `authorization` | [`AuthorizationModel \| undefined`](../../doc/models/authorization-model.md) | Optional | - |

## Example (as JSON)

```json
{
  "IsAuthorized": false,
  "AuthorizationAmount": 186.44,
  "Authorization": null
}
```

