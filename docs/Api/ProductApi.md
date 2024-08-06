# OpenAPI\Client\ProductApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfProductCollectionExistsV1ProductCollectionExistsGet()**](ProductApi.md#checkIfProductCollectionExistsV1ProductCollectionExistsGet) | **GET** /v1/product/collection-exists | Check If Product Collection Exists. |
| [**createProductBySKUV1ProductSkuPost()**](ProductApi.md#createProductBySKUV1ProductSkuPost) | **POST** /v1/product/{sku} | Create Product By Sku |
| [**createProductCollectionV1ProductCollectionPost()**](ProductApi.md#createProductCollectionV1ProductCollectionPost) | **POST** /v1/product/collection | Create Product Collection |
| [**deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete()**](ProductApi.md#deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete) | **DELETE** /v1/product/by-internal-id/{internal_id} | Delete Product By Internal Id |
| [**deleteProductBySKUV1ProductSkuDelete()**](ProductApi.md#deleteProductBySKUV1ProductSkuDelete) | **DELETE** /v1/product/{sku} | Delete Product By Sku |
| [**deleteProductCollectionV1ProductCollectionDelete()**](ProductApi.md#deleteProductCollectionV1ProductCollectionDelete) | **DELETE** /v1/product/collection | Delete Product Collection |
| [**deletesAllProductsFromCollectionV1ProductResetCollectionDelete()**](ProductApi.md#deletesAllProductsFromCollectionV1ProductResetCollectionDelete) | **DELETE** /v1/product/reset-collection | Deletes All Products From Collection |
| [**gestProductBySKUV1ProductSkuGet()**](ProductApi.md#gestProductBySKUV1ProductSkuGet) | **GET** /v1/product/{sku} | Gest Product By Sku |
| [**getAllProductsV1ProductGet()**](ProductApi.md#getAllProductsV1ProductGet) | **GET** /v1/product | Get All Products |
| [**importMultipleProductsV1ProductPost()**](ProductApi.md#importMultipleProductsV1ProductPost) | **POST** /v1/product | Import Multiple Products |
| [**updateProductBySKUV1ProductSkuPut()**](ProductApi.md#updateProductBySKUV1ProductSkuPut) | **PUT** /v1/product/{sku} | Update Product By Sku |


## `checkIfProductCollectionExistsV1ProductCollectionExistsGet()`

```php
checkIfProductCollectionExistsV1ProductCollectionExistsGet(): mixed
```

Check If Product Collection Exists.

Returns true if product collection exists else return false

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
    $result = $apiInstance->checkIfProductCollectionExistsV1ProductCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->checkIfProductCollectionExistsV1ProductCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `createProductBySKUV1ProductSkuPost()`

```php
createProductBySKUV1ProductSkuPost($sku, $product): \OpenAPI\Client\Model\Product
```

Create Product By Sku

Create Product by SKU

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
    $result = $apiInstance->createProductBySKUV1ProductSkuPost($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->createProductBySKUV1ProductSkuPost: ', $e->getMessage(), PHP_EOL;
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

## `createProductCollectionV1ProductCollectionPost()`

```php
createProductCollectionV1ProductCollectionPost($delete_existing_collection): mixed
```

Create Product Collection

Creates product collection/schema in Weaviate database

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

## `deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete()`

```php
deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete($internal_id): bool
```

Delete Product By Internal Id

Delete product by internal_id

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
$internal_id = 56; // int

try {
    $result = $apiInstance->deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteProductBySKUV1ProductSkuDelete()`

```php
deleteProductBySKUV1ProductSkuDelete($sku): bool
```

Delete Product By Sku

Delete product by SKU

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
    $result = $apiInstance->deleteProductBySKUV1ProductSkuDelete($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductBySKUV1ProductSkuDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteProductCollectionV1ProductCollectionDelete()`

```php
deleteProductCollectionV1ProductCollectionDelete(): bool
```

Delete Product Collection

Delete product collection

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

## `deletesAllProductsFromCollectionV1ProductResetCollectionDelete()`

```php
deletesAllProductsFromCollectionV1ProductResetCollectionDelete($dry_run): mixed
```

Deletes All Products From Collection

Deletes all products from the Weaviate product.

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
    $result = $apiInstance->deletesAllProductsFromCollectionV1ProductResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deletesAllProductsFromCollectionV1ProductResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `gestProductBySKUV1ProductSkuGet()`

```php
gestProductBySKUV1ProductSkuGet($sku): \OpenAPI\Client\Model\Product
```

Gest Product By Sku

Get Product by SKU

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
    $result = $apiInstance->gestProductBySKUV1ProductSkuGet($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->gestProductBySKUV1ProductSkuGet: ', $e->getMessage(), PHP_EOL;
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

## `importMultipleProductsV1ProductPost()`

```php
importMultipleProductsV1ProductPost($product): mixed
```

Import Multiple Products

Import multiple products. If a product already exist, it is update. Otherwise new product is created

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
    $result = $apiInstance->importMultipleProductsV1ProductPost($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->importMultipleProductsV1ProductPost: ', $e->getMessage(), PHP_EOL;
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

## `updateProductBySKUV1ProductSkuPut()`

```php
updateProductBySKUV1ProductSkuPut($sku, $product): \OpenAPI\Client\Model\Product
```

Update Product By Sku

Update Product By SKU

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
    $result = $apiInstance->updateProductBySKUV1ProductSkuPut($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->updateProductBySKUV1ProductSkuPut: ', $e->getMessage(), PHP_EOL;
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
