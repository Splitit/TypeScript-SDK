
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | `Environment` | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](../doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| oAuth2SandboxCredentials | [`OAuth2SandboxCredentials`](auth/oauth-2-client-credentials-grant.md) | The credential object for oAuth2Sandbox |
| oAuth2ProductionCredentials | [`OAuth2ProductionCredentials`](auth/oauth-2-client-credentials-grant-1.md) | The credential object for oAuth2Production |

The API client can be initialized as follows:

```ts
import {
  Client,
  Environment,
  OAuthScopeOAuth2ProductionEnum,
  OAuthScopeOAuth2SandboxEnum,
} from 'splitit-payments-sdk';

const client = new Client({
  oAuth2SandboxCredentials: {
    oAuthClientId: 'OAuthClientId',
    oAuthClientSecret: 'OAuthClientSecret',
    oAuthScopes: [
      OAuthScopeOAuth2SandboxEnum.ApiV3
    ]
  },
  oAuth2ProductionCredentials: {
    oAuthClientId: 'OAuthClientId',
    oAuthClientSecret: 'OAuthClientSecret',
    oAuthScopes: [
      OAuthScopeOAuth2ProductionEnum.ApiV3
    ]
  },
  timeout: 0,
  environment: Environment.Production,
});
```

