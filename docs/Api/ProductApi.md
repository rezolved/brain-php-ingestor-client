# OpenAPI\Client\ProductApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProductCollectionV1ProductCollectionPost()**](ProductApi.md#createProductCollectionV1ProductCollectionPost) | **POST** /v1/product/collection | Create Product Collection |
| [**deleteProductCollectionV1ProductCollectionDelete()**](ProductApi.md#deleteProductCollectionV1ProductCollectionDelete) | **DELETE** /v1/product/collection | Delete Product Collection |
| [**getAllProductsV1ProductGet()**](ProductApi.md#getAllProductsV1ProductGet) | **GET** /v1/product | Get All Products |
| [**getProductCollectionV1ProductResetCollectionDelete()**](ProductApi.md#getProductCollectionV1ProductResetCollectionDelete) | **DELETE** /v1/product/reset-collection | Get Product Collection |
| [**getProductV1ProductSkuGet()**](ProductApi.md#getProductV1ProductSkuGet) | **GET** /v1/product/{sku} | Get Product |
| [**ingestProductV1ProductSkuPost()**](ProductApi.md#ingestProductV1ProductSkuPost) | **POST** /v1/product/{sku} | Ingest Product |
| [**ingestProductV1ProductSkuPut()**](ProductApi.md#ingestProductV1ProductSkuPut) | **PUT** /v1/product/{sku} | Ingest Product |
| [**ingestProductsV1ProductPost()**](ProductApi.md#ingestProductsV1ProductPost) | **POST** /v1/product | Ingest Products |


## `createProductCollectionV1ProductCollectionPost()`

```php
createProductCollectionV1ProductCollectionPost($delete_existing_collection): mixed
```

Create Product Collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delete_existing_collection = false; // bool

try {
    $result = $apiInstance->createProductCollectionV1ProductCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->createProductCollectionV1ProductCollectionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delete_existing_collection** | **bool**|  | [optional] [default to false] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProductCollectionV1ProductCollectionDelete()`

```php
deleteProductCollectionV1ProductCollectionDelete(): bool
```

Delete Product Collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteProductCollectionV1ProductCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductCollectionV1ProductCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `getAllProductsV1ProductGet()`

```php
getAllProductsV1ProductGet(): \OpenAPI\Client\Model\Product[]
```

Get All Products

Returns All Products. If collection has a large number of products, response may take long time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllProductsV1ProductGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getAllProductsV1ProductGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Product[]**](../Model/Product.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductCollectionV1ProductResetCollectionDelete()`

```php
getProductCollectionV1ProductResetCollectionDelete($dry_run): mixed
```

Get Product Collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dry_run = true; // bool

try {
    $result = $apiInstance->getProductCollectionV1ProductResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getProductCollectionV1ProductResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dry_run** | **bool**|  | [optional] [default to true] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductV1ProductSkuGet()`

```php
getProductV1ProductSkuGet($sku): \OpenAPI\Client\Model\Product
```

Get Product

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string

try {
    $result = $apiInstance->getProductV1ProductSkuGet($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getProductV1ProductSkuGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Product**](../Model/Product.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ingestProductV1ProductSkuPost()`

```php
ingestProductV1ProductSkuPost($sku, $product): \OpenAPI\Client\Model\Product
```

Ingest Product

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string
$product = new \OpenAPI\Client\Model\Product(); // \OpenAPI\Client\Model\Product

try {
    $result = $apiInstance->ingestProductV1ProductSkuPost($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->ingestProductV1ProductSkuPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |
| **product** | [**\OpenAPI\Client\Model\Product**](../Model/Product.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Product**](../Model/Product.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ingestProductV1ProductSkuPut()`

```php
ingestProductV1ProductSkuPut($sku, $product): \OpenAPI\Client\Model\Product
```

Ingest Product

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string
$product = new \OpenAPI\Client\Model\Product(); // \OpenAPI\Client\Model\Product

try {
    $result = $apiInstance->ingestProductV1ProductSkuPut($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->ingestProductV1ProductSkuPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |
| **product** | [**\OpenAPI\Client\Model\Product**](../Model/Product.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Product**](../Model/Product.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ingestProductsV1ProductPost()`

```php
ingestProductsV1ProductPost($product): mixed
```

Ingest Products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product = array(new \OpenAPI\Client\Model\Product()); // \OpenAPI\Client\Model\Product[]

try {
    $result = $apiInstance->ingestProductsV1ProductPost($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->ingestProductsV1ProductPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product** | [**\OpenAPI\Client\Model\Product[]**](../Model/Product.md)|  | |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
