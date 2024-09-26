# OpenAPI\Client\ReviewsApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet()**](ReviewsApi.md#checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet) | **GET** /v1/reviews/is-schema-exists | Check If Product Review Schema Exists |
| [**createOneReviewBySKUV1ReviewsPost()**](ReviewsApi.md#createOneReviewBySKUV1ReviewsPost) | **POST** /v1/reviews | Create One Review By Sku |
| [**createSchemaAndProductReviewTableV1ReviewsSchemaPost()**](ReviewsApi.md#createSchemaAndProductReviewTableV1ReviewsSchemaPost) | **POST** /v1/reviews/schema | Create Schema And Product Review Table |
| [**deleteAllReviewsV1ReviewsDelete()**](ReviewsApi.md#deleteAllReviewsV1ReviewsDelete) | **DELETE** /v1/reviews/ | Delete All Reviews |
| [**deleteReviewsByProductSKUV1ReviewsSkuDelete()**](ReviewsApi.md#deleteReviewsByProductSKUV1ReviewsSkuDelete) | **DELETE** /v1/reviews/{sku} | Delete Reviews By Product Sku |
| [**deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete()**](ReviewsApi.md#deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete) | **DELETE** /v1/reviews/by-internal-id/{internal_id} | Delete Single Review By Internal Id |
| [**getAllReviewsV1ReviewsGet()**](ReviewsApi.md#getAllReviewsV1ReviewsGet) | **GET** /v1/reviews | Get All Reviews |
| [**getReviewsBySKUV1ReviewsSkuGet()**](ReviewsApi.md#getReviewsBySKUV1ReviewsSkuGet) | **GET** /v1/reviews/{sku} | Get Reviews By Sku |
| [**importMultipleReviewsV1ReviewsImportPost()**](ReviewsApi.md#importMultipleReviewsV1ReviewsImportPost) | **POST** /v1/reviews/import | Import Multiple Reviews |


## `checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet()`

```php
checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet(): bool
```

Check If Product Review Schema Exists

Check if product review schema exists

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->checkIfProductReviewSchemaExistsV1ReviewsIsSchemaExistsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createOneReviewBySKUV1ReviewsPost()`

```php
createOneReviewBySKUV1ReviewsPost($review): string
```

Create One Review By Sku

Create One Review by SKU

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$review = new \OpenAPI\Client\Model\Review(); // \OpenAPI\Client\Model\Review

try {
    $result = $apiInstance->createOneReviewBySKUV1ReviewsPost($review);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->createOneReviewBySKUV1ReviewsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **review** | [**\OpenAPI\Client\Model\Review**](../Model/Review.md)|  | |

### Return type

**string**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSchemaAndProductReviewTableV1ReviewsSchemaPost()`

```php
createSchemaAndProductReviewTableV1ReviewsSchemaPost(): bool
```

Create Schema And Product Review Table

Create Schema And Product Review table

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->createSchemaAndProductReviewTableV1ReviewsSchemaPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->createSchemaAndProductReviewTableV1ReviewsSchemaPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteAllReviewsV1ReviewsDelete()`

```php
deleteAllReviewsV1ReviewsDelete(): bool
```

Delete All Reviews

Delete all reviews from table

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteAllReviewsV1ReviewsDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->deleteAllReviewsV1ReviewsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteReviewsByProductSKUV1ReviewsSkuDelete()`

```php
deleteReviewsByProductSKUV1ReviewsSkuDelete($sku): bool
```

Delete Reviews By Product Sku

Delete all reviews related to the product SKU

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string

try {
    $result = $apiInstance->deleteReviewsByProductSKUV1ReviewsSkuDelete($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->deleteReviewsByProductSKUV1ReviewsSkuDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete()`

```php
deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete($internal_id): bool
```

Delete Single Review By Internal Id

Delete single review by internal_id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$internal_id = 56; // int

try {
    $result = $apiInstance->deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->deleteSingleReviewByInternalIdV1ReviewsByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **internal_id** | **int**|  | |

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllReviewsV1ReviewsGet()`

```php
getAllReviewsV1ReviewsGet(): mixed[]
```

Get All Reviews

Returns All Reviews. If collection has a large number of products, response may take long time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllReviewsV1ReviewsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->getAllReviewsV1ReviewsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed[]**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReviewsBySKUV1ReviewsSkuGet()`

```php
getReviewsBySKUV1ReviewsSkuGet($sku): mixed[]
```

Get Reviews By Sku

Get Reviews by SKU

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string

try {
    $result = $apiInstance->getReviewsBySKUV1ReviewsSkuGet($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->getReviewsBySKUV1ReviewsSkuGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |

### Return type

**mixed[]**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `importMultipleReviewsV1ReviewsImportPost()`

```php
importMultipleReviewsV1ReviewsImportPost($review): bool
```

Import Multiple Reviews

Import multiple reviews data. Better to cleanup reviews for specific product sku and then add multiple reviews.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ReviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$review = array(new \OpenAPI\Client\Model\Review()); // \OpenAPI\Client\Model\Review[]

try {
    $result = $apiInstance->importMultipleReviewsV1ReviewsImportPost($review);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewsApi->importMultipleReviewsV1ReviewsImportPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **review** | [**\OpenAPI\Client\Model\Review[]**](../Model/Review.md)|  | |

### Return type

**bool**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
