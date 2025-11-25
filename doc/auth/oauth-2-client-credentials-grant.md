
# OAuth 2 Client Credentials Grant



Documentation for accessing and setting credentials for OAuth2-sandbox.

## Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| OAuthClientId | `string` | OAuth 2 Client ID | `oAuthClientId` |
| OAuthClientSecret | `string` | OAuth 2 Client Secret | `oAuthClientSecret` |
| OAuthToken | `OAuthToken` | Object for storing information about the OAuth token | `oAuthToken` |
| OAuthScopes | `OAuthScopeOAuth2SandboxEnum[]` | List of scopes that apply to the OAuth token | `oAuthScopes` |
| OAuthClockSkew | `number` | Clock skew time in seconds applied while checking the OAuth Token expiry. | `clockSkew` |
| OAuthTokenProvider | `(lastOAuthToken: OAuthToken \| undefined, authManager: OAuth2SandboxManager) => Promise<OAuthToken>` | Registers a callback for oAuth Token Provider used for automatic token fetching/refreshing. | `oAuthTokenProvider` |
| OAuthOnTokenUpdate | `(token: OAuthToken) => void` | Registers a callback for token update event. | `oAuthOnTokenUpdate` |



**Note:** Auth credentials can be set using `oAuth2SandboxCredentials` object in the client.

## Usage Example

### Client Initialization

You must initialize the client with *OAuth 2.0 Client Credentials Grant* credentials as shown in the following code snippet. This will fetch the OAuth token automatically when any of the endpoints, requiring *OAuth 2.0 Client Credentials Grant* authentication, are called.

```ts
import { Client, OAuthScopeOAuth2SandboxEnum } from 'splitit-payments-sdk';

const client = new Client({
  oAuth2SandboxCredentials: {
    oAuthClientId: 'OAuthClientId',
    oAuthClientSecret: 'OAuthClientSecret',
    oAuthScopes: [
      OAuthScopeOAuth2SandboxEnum.ApiV3
    ]
  },
});
```



Your application can also manually provide an OAuthToken using the setter `oAuthToken` in `oAuth2SandboxCredentials` object. This function takes in an instance of OAuthToken containing information for authorizing client requests and refreshing the token itself.

You must have initialized the client with scopes for which you need permission to access.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeOAuth2SandboxEnum`](../../doc/models/o-auth-scope-o-auth-2-sandbox-enum.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `ApiV3` | Access to WebAPI version 3 |

### Adding OAuth Token Update Callback

Whenever the OAuth Token gets updated, the provided callback implementation will be executed. For instance, you may use it to store your access token whenever it gets updated.

```ts
import {
  Client,
  OAuthScopeOAuth2SandboxEnum,
  OAuthToken,
} from 'splitit-payments-sdk';

const client = new Client({
  oAuth2SandboxCredentials: {
    oAuthClientId: 'OAuthClientId',
    oAuthClientSecret: 'OAuthClientSecret',
    oAuthScopes: [
      OAuthScopeOAuth2SandboxEnum.ApiV3
    ],
    oAuthOnTokenUpdate: (token: OAuthToken) => {
      // Add the callback handler to perform operations like save to DB or file etc.
      // It will be triggered whenever the token gets updated
      saveTokenToDatabase(token);
    }
  },
});
```

### Adding Custom OAuth Token Provider

To authorize a client using a stored access token, set up the `oAuthTokenProvider` in `oAuth2SandboxCredentials` along with the other auth parameters before creating the client:

```ts
import {
  Client,
  OAuth2SandboxManager,
  OAuthScopeOAuth2SandboxEnum,
  OAuthToken,
} from 'splitit-payments-sdk';

const client = new Client({
  oAuth2SandboxCredentials: {
    oAuthClientId: 'OAuthClientId',
    oAuthClientSecret: 'OAuthClientSecret',
    oAuthScopes: [
      OAuthScopeOAuth2SandboxEnum.ApiV3
    ],
    oAuthTokenProvider: (lastOAuthToken: OAuthToken | undefined, authManager: OAuth2SandboxManager) => {
      // Add the callback handler to provide a new OAuth token
      // It will be triggered whenever the lastOAuthToken is undefined or expired
      return loadTokenFromDatabase() ?? authManager.fetchToken();
    }
  },
});
```


