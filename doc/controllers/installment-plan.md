# Installment Plan

```ts
const installmentPlanController = new InstallmentPlanController(client);
```

## Class Name

`InstallmentPlanController`

## Methods

* [Installment Plan Get](../../doc/controllers/installment-plan.md#installment-plan-get)
* [Installment Plan Search](../../doc/controllers/installment-plan.md#installment-plan-search)
* [Installment Plan Post](../../doc/controllers/installment-plan.md#installment-plan-post)
* [Installment Plan Post 2](../../doc/controllers/installment-plan.md#installment-plan-post-2)
* [Installment Plan Verify Authorization](../../doc/controllers/installment-plan.md#installment-plan-verify-authorization)
* [Installment Plan Update Order](../../doc/controllers/installment-plan.md#installment-plan-update-order)
* [Installment Plan Update Order 2](../../doc/controllers/installment-plan.md#installment-plan-update-order-2)
* [Installment Plan Refund](../../doc/controllers/installment-plan.md#installment-plan-refund)
* [Installment Plan Check Eligibility](../../doc/controllers/installment-plan.md#installment-plan-check-eligibility)
* [Installment Plan Get Eligibility Terms and Condition](../../doc/controllers/installment-plan.md#installment-plan-get-eligibility-terms-and-condition)


# Installment Plan Get

```ts
async installmentPlanGet(
  installmentPlanNumber: string,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanGetResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string` | Template, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanGetResponse`](../../doc/models/installment-plan-get-response.md).

## Example Usage

```ts
const installmentPlanNumber = 'installmentPlanNumber6';

try {
  const response = await installmentPlanController.installmentPlanGet(installmentPlanNumber);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Search

```ts
async installmentPlanSearch(
  installmentPlanNumber?: string | null,
  refOrderNumber?: string | null,
  extendedParams?: unknown | null,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanSearchResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string \| null \| undefined` | Query, Optional | - |
| `refOrderNumber` | `string \| null \| undefined` | Query, Optional | - |
| `extendedParams` | `unknown \| null \| undefined` | Query, Optional | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanSearchResponse`](../../doc/models/installment-plan-search-response.md).

## Example Usage

```ts
try {
  const response = await installmentPlanController.installmentPlanSearch();

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Post

```ts
async installmentPlanPost(
  xSplititIdempotencyKey: string,
  body: InstallmentPlanInitiateRequest,
  xSplititTestMode?: TestModesEnum | null,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InitiatePlanResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`InstallmentPlanInitiateRequest`](../../doc/models/installment-plan-initiate-request.md) | Body, Required | - |
| `xSplititTestMode` | [`TestModesEnum \| null \| undefined`](../../doc/models/test-modes-enum.md) | Header, Optional | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InitiatePlanResponse`](../../doc/models/initiate-plan-response.md).

## Example Usage

```ts
const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: InstallmentPlanInitiateRequest = {
};

try {
  const response = await installmentPlanController.installmentPlanPost(
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | - | [`PlanErrorResponseError`](../../doc/models/plan-error-response-error.md) |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Post 2

```ts
async installmentPlanPost2(
  xSplititIdempotencyKey: string,
  body: InstallmentPlanCreateRequest,
  xSplititTestMode?: TestModesEnum | null,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanCreateResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`InstallmentPlanCreateRequest`](../../doc/models/installment-plan-create-request.md) | Body, Required | - |
| `xSplititTestMode` | [`TestModesEnum \| null \| undefined`](../../doc/models/test-modes-enum.md) | Header, Optional | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanCreateResponse`](../../doc/models/installment-plan-create-response.md).

## Example Usage

```ts
const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: InstallmentPlanCreateRequest = {
  autoCapture: false,
  termsAndConditionsAccepted: false,
};

try {
  const response = await installmentPlanController.installmentPlanPost2(
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | - | [`PlanErrorResponseError`](../../doc/models/plan-error-response-error.md) |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Verify Authorization

```ts
async installmentPlanVerifyAuthorization(
  installmentPlanNumber: string,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<VerifyAuthorizationResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string` | Template, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`VerifyAuthorizationResponse`](../../doc/models/verify-authorization-response.md).

## Example Usage

```ts
const installmentPlanNumber = 'installmentPlanNumber6';

try {
  const response = await installmentPlanController.installmentPlanVerifyAuthorization(installmentPlanNumber);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Update Order

```ts
async installmentPlanUpdateOrder(
  installmentPlanNumber: string,
  xSplititIdempotencyKey: string,
  body: InstallmentPlanUpdateRequest,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanUpdateResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string` | Template, Required | - |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`InstallmentPlanUpdateRequest`](../../doc/models/installment-plan-update-request.md) | Body, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanUpdateResponse`](../../doc/models/installment-plan-update-response.md).

## Example Usage

```ts
const installmentPlanNumber = 'installmentPlanNumber6';

const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: InstallmentPlanUpdateRequest = {
};

try {
  const response = await installmentPlanController.installmentPlanUpdateOrder(
    installmentPlanNumber,
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Update Order 2

```ts
async installmentPlanUpdateOrder2(
  xSplititIdempotencyKey: string,
  body: InstallmentPlanUpdateRequestByIdentifier,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanUpdateResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`InstallmentPlanUpdateRequestByIdentifier`](../../doc/models/installment-plan-update-request-by-identifier.md) | Body, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanUpdateResponse`](../../doc/models/installment-plan-update-response.md).

## Example Usage

```ts
const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: InstallmentPlanUpdateRequestByIdentifier = {
};

try {
  const response = await installmentPlanController.installmentPlanUpdateOrder2(
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Refund

```ts
async installmentPlanRefund(
  installmentPlanNumber: string,
  xSplititIdempotencyKey: string,
  body: InstallmentPlanRefundRequest,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentPlanRefundResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installmentPlanNumber` | `string` | Template, Required | - |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`InstallmentPlanRefundRequest`](../../doc/models/installment-plan-refund-request.md) | Body, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentPlanRefundResponse`](../../doc/models/installment-plan-refund-response.md).

## Example Usage

```ts
const installmentPlanNumber = 'installmentPlanNumber6';

const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: InstallmentPlanRefundRequest = {
  amount: 'Amount8',
};

try {
  const response = await installmentPlanController.installmentPlanRefund(
    installmentPlanNumber,
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Check Eligibility

```ts
async installmentPlanCheckEligibility(
  xSplititIdempotencyKey: string,
  body: CheckInstallmentsEligibilityRequest,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<InstallmentsEligibilityResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xSplititIdempotencyKey` | `string` | Header, Required | - |
| `body` | [`CheckInstallmentsEligibilityRequest`](../../doc/models/check-installments-eligibility-request.md) | Body, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`InstallmentsEligibilityResponse`](../../doc/models/installments-eligibility-response.md).

## Example Usage

```ts
const xSplititIdempotencyKey = 'X-Splitit-IdempotencyKey2';

const body: CheckInstallmentsEligibilityRequest = {
};

try {
  const response = await installmentPlanController.installmentPlanCheckEligibility(
    xSplititIdempotencyKey,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |


# Installment Plan Get Eligibility Terms and Condition

```ts
async installmentPlanGetEligibilityTermsAndCondition(
  ipn: string,
  xSplititTouchPoint?: string | null,
  requestOptions?: RequestOptions
): Promise<ApiResponse<EligibilityTermsAndConditionResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipn` | `string` | Template, Required | - |
| `xSplititTouchPoint` | `string \| null \| undefined` | Header, Optional | TouchPoint |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Requires scope

### OAuth2-sandbox

`api.v3`

### OAuth2-production

`api.v3`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`EligibilityTermsAndConditionResponse`](../../doc/models/eligibility-terms-and-condition-response.md).

## Example Usage

```ts
const ipn = 'ipn4';

try {
  const response = await installmentPlanController.installmentPlanGetEligibilityTermsAndCondition(ipn);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 403 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 404 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |
| 500 | - | [`FailedResponseError`](../../doc/models/failed-response-error.md) |

