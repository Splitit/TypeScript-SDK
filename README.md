
# Getting Started with splitit-web-api-v3

## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install splitit-payments-sdk@1.0.7
```

For additional package details, see the [Npm page for the splitit-payments-sdk@1.0.7 npm](https://www.npmjs.com/package/splitit-payments-sdk/v/1.0.7).

## Test the SDK

To validate the functionality of this SDK, you can execute all tests located in the `test` directory. This SDK utilizes `Jest` as both the testing framework and test runner.

To run the tests, navigate to the root directory of the SDK and execute the following command:

```bash
npm run test
```

Or you can also run tests with coverage report:

```bash
npm run test:coverage
```

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | `Environment` | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| oAuth2SandboxCredentials | [`OAuth2SandboxCredentials`](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/auth/oauth-2-client-credentials-grant.md) | The credential object for oAuth2Sandbox |
| oAuth2ProductionCredentials | [`OAuth2ProductionCredentials`](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/auth/oauth-2-client-credentials-grant-1.md) | The credential object for oAuth2Production |

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

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| production | **Default** Sandbox |
| environment2 | Production |

## Authorization

This API uses the following authentication schemes.

* [`OAuth2-sandbox (OAuth 2 Client Credentials Grant)`](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/auth/oauth-2-client-credentials-grant.md)
* [`OAuth2-production (OAuth 2 Client Credentials Grant)`](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/auth/oauth-2-client-credentials-grant-1.md)

## List of APIs

* [Installment Plan](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/controllers/installment-plan.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/http-client-options.md)
* [RetryConfiguration](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/retry-configuration.md)
* [ProxySettings](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/proxy-settings.md)

### HTTP

* [HttpRequest](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/api-response.md)
* [ApiError](https://www.github.com/Splitit/TypeScript-SDK/tree/1.0.7/doc/api-error.md)

