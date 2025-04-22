# OpenAPI\Client\ProductApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfProductCollectionExistsV1ProductsCollectionExistsGet()**](ProductApi.md#checkIfProductCollectionExistsV1ProductsCollectionExistsGet) | **GET** /v1/products/collection-exists | Check If Product Collection Exists. |
| [**createProductBySKUV1ProductsSkuPost()**](ProductApi.md#createProductBySKUV1ProductsSkuPost) | **POST** /v1/products/{sku} | Create Product By Sku |
| [**createProductCollectionV1ProductsCollectionPost()**](ProductApi.md#createProductCollectionV1ProductsCollectionPost) | **POST** /v1/products/collection | Create Product Collection |
| [**deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete()**](ProductApi.md#deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete) | **DELETE** /v1/products/by-internal-id/{internal_id} | Delete Product By Internal Id |
| [**deleteProductBySKUV1ProductsSkuDelete()**](ProductApi.md#deleteProductBySKUV1ProductsSkuDelete) | **DELETE** /v1/products/{sku} | Delete Product By Sku |
| [**deleteProductCollectionV1ProductsCollectionDelete()**](ProductApi.md#deleteProductCollectionV1ProductsCollectionDelete) | **DELETE** /v1/products/collection | Delete Product Collection |
| [**deletesAllProductsFromCollectionV1ProductsResetCollectionDelete()**](ProductApi.md#deletesAllProductsFromCollectionV1ProductsResetCollectionDelete) | **DELETE** /v1/products/reset-collection | Deletes All Products From Collection |
| [**gestProductBySKUV1ProductsSkuGet()**](ProductApi.md#gestProductBySKUV1ProductsSkuGet) | **GET** /v1/products/{sku} | Gest Product By Sku |
| [**getAllProductsV1ProductsGet()**](ProductApi.md#getAllProductsV1ProductsGet) | **GET** /v1/products | Get All Products |
| [**importMultipleProductsV1ProductsPost()**](ProductApi.md#importMultipleProductsV1ProductsPost) | **POST** /v1/products | Import Multiple Products |
| [**updateProductBySKUV1ProductsSkuPut()**](ProductApi.md#updateProductBySKUV1ProductsSkuPut) | **PUT** /v1/products/{sku} | Update Product By Sku |
| [**uploadFilesIntoStorageV1ProductsUploadPost()**](ProductApi.md#uploadFilesIntoStorageV1ProductsUploadPost) | **POST** /v1/products/upload/ | Upload Files Into Storage |


## `checkIfProductCollectionExistsV1ProductsCollectionExistsGet()`

```php
checkIfProductCollectionExistsV1ProductsCollectionExistsGet(): mixed
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
    $result = $apiInstance->checkIfProductCollectionExistsV1ProductsCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->checkIfProductCollectionExistsV1ProductsCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createProductBySKUV1ProductsSkuPost()`

```php
createProductBySKUV1ProductsSkuPost($sku, $product): \OpenAPI\Client\Model\Product
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
    $result = $apiInstance->createProductBySKUV1ProductsSkuPost($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->createProductBySKUV1ProductsSkuPost: ', $e->getMessage(), PHP_EOL;
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

## `createProductCollectionV1ProductsCollectionPost()`

```php
createProductCollectionV1ProductsCollectionPost($delete_existing_collection): mixed
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
    $result = $apiInstance->createProductCollectionV1ProductsCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->createProductCollectionV1ProductsCollectionPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete()`

```php
deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete($internal_id): bool
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
    $result = $apiInstance->deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductByInternalIdV1ProductsByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteProductBySKUV1ProductsSkuDelete()`

```php
deleteProductBySKUV1ProductsSkuDelete($sku): bool
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
    $result = $apiInstance->deleteProductBySKUV1ProductsSkuDelete($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductBySKUV1ProductsSkuDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteProductCollectionV1ProductsCollectionDelete()`

```php
deleteProductCollectionV1ProductsCollectionDelete(): bool
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
    $result = $apiInstance->deleteProductCollectionV1ProductsCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deleteProductCollectionV1ProductsCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deletesAllProductsFromCollectionV1ProductsResetCollectionDelete()`

```php
deletesAllProductsFromCollectionV1ProductsResetCollectionDelete($dry_run): mixed
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
    $result = $apiInstance->deletesAllProductsFromCollectionV1ProductsResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->deletesAllProductsFromCollectionV1ProductsResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `gestProductBySKUV1ProductsSkuGet()`

```php
gestProductBySKUV1ProductsSkuGet($sku): \OpenAPI\Client\Model\Product
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
    $result = $apiInstance->gestProductBySKUV1ProductsSkuGet($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->gestProductBySKUV1ProductsSkuGet: ', $e->getMessage(), PHP_EOL;
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

## `getAllProductsV1ProductsGet()`

```php
getAllProductsV1ProductsGet(): \OpenAPI\Client\Model\Product[]
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
    $result = $apiInstance->getAllProductsV1ProductsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getAllProductsV1ProductsGet: ', $e->getMessage(), PHP_EOL;
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

## `importMultipleProductsV1ProductsPost()`

```php
importMultipleProductsV1ProductsPost($product): mixed
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
    $result = $apiInstance->importMultipleProductsV1ProductsPost($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->importMultipleProductsV1ProductsPost: ', $e->getMessage(), PHP_EOL;
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

## `updateProductBySKUV1ProductsSkuPut()`

```php
updateProductBySKUV1ProductsSkuPut($sku, $product): \OpenAPI\Client\Model\Product
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
    $result = $apiInstance->updateProductBySKUV1ProductsSkuPut($sku, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->updateProductBySKUV1ProductsSkuPut: ', $e->getMessage(), PHP_EOL;
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

## `uploadFilesIntoStorageV1ProductsUploadPost()`

```php
uploadFilesIntoStorageV1ProductsUploadPost($file): object
```

Upload Files Into Storage

Upload files to Cloud Storage.

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
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadFilesIntoStorageV1ProductsUploadPost($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->uploadFilesIntoStorageV1ProductsUploadPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**|  | |

### Return type

**object**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
