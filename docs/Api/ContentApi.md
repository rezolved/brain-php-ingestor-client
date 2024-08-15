# OpenAPI\Client\ContentApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfContentCollectionExistsV1ContentCollectionExistsGet()**](ContentApi.md#checkIfContentCollectionExistsV1ContentCollectionExistsGet) | **GET** /v1/content/collection-exists | Check If Content Collection Exists. |
| [**createContentByTitleV1ContentTitlePost()**](ContentApi.md#createContentByTitleV1ContentTitlePost) | **POST** /v1/content/{title} | Create Content By Title |
| [**createContentCollectionV1ContentCollectionPost()**](ContentApi.md#createContentCollectionV1ContentCollectionPost) | **POST** /v1/content/collection | Create Content Collection |
| [**deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete()**](ContentApi.md#deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete) | **DELETE** /v1/content/by-internal-id/{internal_id} | Delete Content By Internal Id |
| [**deleteContentByTitleV1ContentTitleDelete()**](ContentApi.md#deleteContentByTitleV1ContentTitleDelete) | **DELETE** /v1/content/{title} | Delete Content By Title |
| [**deleteContentCollectionV1ContentCollectionDelete()**](ContentApi.md#deleteContentCollectionV1ContentCollectionDelete) | **DELETE** /v1/content/collection | Delete Content Collection |
| [**deletesAllContentFromCollectionV1ContentResetCollectionDelete()**](ContentApi.md#deletesAllContentFromCollectionV1ContentResetCollectionDelete) | **DELETE** /v1/content/reset-collection | Deletes All Content From Collection |
| [**gestContentByTitleV1ContentTitleGet()**](ContentApi.md#gestContentByTitleV1ContentTitleGet) | **GET** /v1/content/{title} | Gest Content By Title |
| [**getAllContentsV1ContentGet()**](ContentApi.md#getAllContentsV1ContentGet) | **GET** /v1/content | Get All Contents |
| [**importMultipleContentsV1ContentPost()**](ContentApi.md#importMultipleContentsV1ContentPost) | **POST** /v1/content | Import Multiple Contents |
| [**updateContentByTitleV1ContentTitlePut()**](ContentApi.md#updateContentByTitleV1ContentTitlePut) | **PUT** /v1/content/{title} | Update Content By Title |


## `checkIfContentCollectionExistsV1ContentCollectionExistsGet()`

```php
checkIfContentCollectionExistsV1ContentCollectionExistsGet(): mixed
```

Check If Content Collection Exists.

Returns true if content collection exists else return false

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->checkIfContentCollectionExistsV1ContentCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->checkIfContentCollectionExistsV1ContentCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createContentByTitleV1ContentTitlePost()`

```php
createContentByTitleV1ContentTitlePost($title, $content): \OpenAPI\Client\Model\Content
```

Create Content By Title

Create content by title

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$title = 'title_example'; // string
$content = new \OpenAPI\Client\Model\Content(); // \OpenAPI\Client\Model\Content

try {
    $result = $apiInstance->createContentByTitleV1ContentTitlePost($title, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->createContentByTitleV1ContentTitlePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **title** | **string**|  | |
| **content** | [**\OpenAPI\Client\Model\Content**](../Model/Content.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Content**](../Model/Content.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createContentCollectionV1ContentCollectionPost()`

```php
createContentCollectionV1ContentCollectionPost($delete_existing_collection): mixed
```

Create Content Collection

Creates content collection/schema in Weaviate database

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delete_existing_collection = false; // bool

try {
    $result = $apiInstance->createContentCollectionV1ContentCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->createContentCollectionV1ContentCollectionPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete()`

```php
deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete($internal_id): bool
```

Delete Content By Internal Id

Delete content by internal_id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$internal_id = 56; // int

try {
    $result = $apiInstance->deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteContentByTitleV1ContentTitleDelete()`

```php
deleteContentByTitleV1ContentTitleDelete($title): bool
```

Delete Content By Title

Delete content by title

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$title = 'title_example'; // string

try {
    $result = $apiInstance->deleteContentByTitleV1ContentTitleDelete($title);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentByTitleV1ContentTitleDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **title** | **string**|  | |

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

## `deleteContentCollectionV1ContentCollectionDelete()`

```php
deleteContentCollectionV1ContentCollectionDelete(): bool
```

Delete Content Collection

Delete content collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteContentCollectionV1ContentCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentCollectionV1ContentCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deletesAllContentFromCollectionV1ContentResetCollectionDelete()`

```php
deletesAllContentFromCollectionV1ContentResetCollectionDelete($dry_run): mixed
```

Deletes All Content From Collection

Deletes all content from collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dry_run = true; // bool

try {
    $result = $apiInstance->deletesAllContentFromCollectionV1ContentResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deletesAllContentFromCollectionV1ContentResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `gestContentByTitleV1ContentTitleGet()`

```php
gestContentByTitleV1ContentTitleGet($title): \OpenAPI\Client\Model\Content
```

Gest Content By Title

Get content by title

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$title = 'title_example'; // string

try {
    $result = $apiInstance->gestContentByTitleV1ContentTitleGet($title);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->gestContentByTitleV1ContentTitleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **title** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Content**](../Model/Content.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllContentsV1ContentGet()`

```php
getAllContentsV1ContentGet(): \OpenAPI\Client\Model\Content[]
```

Get All Contents

Returns All contents. If collection has a large number of contentss, response may take long time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllContentsV1ContentGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->getAllContentsV1ContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Content[]**](../Model/Content.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `importMultipleContentsV1ContentPost()`

```php
importMultipleContentsV1ContentPost($content): mixed
```

Import Multiple Contents

Import multiple Contents. If a content same title already exist, it is updated. Otherwise new content is created

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$content = array(new \OpenAPI\Client\Model\Content()); // \OpenAPI\Client\Model\Content[]

try {
    $result = $apiInstance->importMultipleContentsV1ContentPost($content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->importMultipleContentsV1ContentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **content** | [**\OpenAPI\Client\Model\Content[]**](../Model/Content.md)|  | |

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

## `updateContentByTitleV1ContentTitlePut()`

```php
updateContentByTitleV1ContentTitlePut($title, $content): \OpenAPI\Client\Model\Content
```

Update Content By Title

Update content By title

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$title = 'title_example'; // string
$content = new \OpenAPI\Client\Model\Content(); // \OpenAPI\Client\Model\Content

try {
    $result = $apiInstance->updateContentByTitleV1ContentTitlePut($title, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->updateContentByTitleV1ContentTitlePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **title** | **string**|  | |
| **content** | [**\OpenAPI\Client\Model\Content**](../Model/Content.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Content**](../Model/Content.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
