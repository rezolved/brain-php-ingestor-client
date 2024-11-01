# OpenAPI\Client\ContentApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfContentCollectionExistsV1ContentsCollectionExistsGet()**](ContentApi.md#checkIfContentCollectionExistsV1ContentsCollectionExistsGet) | **GET** /v1/contents/collection-exists | Check If Content Collection Exists. |
| [**createContentByTitleV1ContentsTitlePost()**](ContentApi.md#createContentByTitleV1ContentsTitlePost) | **POST** /v1/contents/{title} | Create Content By Title |
| [**createContentCollectionV1ContentsCollectionPost()**](ContentApi.md#createContentCollectionV1ContentsCollectionPost) | **POST** /v1/contents/collection | Create Content Collection |
| [**deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete()**](ContentApi.md#deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete) | **DELETE** /v1/contents/by-internal-id/{internal_id} | Delete Content By Internal Id |
| [**deleteContentByTitleV1ContentsTitleDelete()**](ContentApi.md#deleteContentByTitleV1ContentsTitleDelete) | **DELETE** /v1/contents/{title} | Delete Content By Title |
| [**deleteContentCollectionV1ContentsCollectionDelete()**](ContentApi.md#deleteContentCollectionV1ContentsCollectionDelete) | **DELETE** /v1/contents/collection | Delete Content Collection |
| [**deletesAllContentFromCollectionV1ContentsResetCollectionDelete()**](ContentApi.md#deletesAllContentFromCollectionV1ContentsResetCollectionDelete) | **DELETE** /v1/contents/reset-collection | Deletes All Content From Collection |
| [**gestContentByTitleV1ContentsTitleGet()**](ContentApi.md#gestContentByTitleV1ContentsTitleGet) | **GET** /v1/contents/{title} | Gest Content By Title |
| [**getAllContentsV1ContentsGet()**](ContentApi.md#getAllContentsV1ContentsGet) | **GET** /v1/contents | Get All Contents |
| [**importMultipleContentsV1ContentsPost()**](ContentApi.md#importMultipleContentsV1ContentsPost) | **POST** /v1/contents | Import Multiple Contents |
| [**updateContentByTitleV1ContentsTitlePut()**](ContentApi.md#updateContentByTitleV1ContentsTitlePut) | **PUT** /v1/contents/{title} | Update Content By Title |
| [**uploadFilesIntoGCSV1ContentsUploadPost()**](ContentApi.md#uploadFilesIntoGCSV1ContentsUploadPost) | **POST** /v1/contents/upload | Upload Files Into Gcs |


## `checkIfContentCollectionExistsV1ContentsCollectionExistsGet()`

```php
checkIfContentCollectionExistsV1ContentsCollectionExistsGet(): mixed
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
    $result = $apiInstance->checkIfContentCollectionExistsV1ContentsCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->checkIfContentCollectionExistsV1ContentsCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createContentByTitleV1ContentsTitlePost()`

```php
createContentByTitleV1ContentsTitlePost($title, $content): \OpenAPI\Client\Model\Content
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
    $result = $apiInstance->createContentByTitleV1ContentsTitlePost($title, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->createContentByTitleV1ContentsTitlePost: ', $e->getMessage(), PHP_EOL;
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

## `createContentCollectionV1ContentsCollectionPost()`

```php
createContentCollectionV1ContentsCollectionPost($delete_existing_collection): mixed
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
    $result = $apiInstance->createContentCollectionV1ContentsCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->createContentCollectionV1ContentsCollectionPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete()`

```php
deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete($internal_id): bool
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
    $result = $apiInstance->deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentByInternalIdV1ContentsByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteContentByTitleV1ContentsTitleDelete()`

```php
deleteContentByTitleV1ContentsTitleDelete($title): bool
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
    $result = $apiInstance->deleteContentByTitleV1ContentsTitleDelete($title);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentByTitleV1ContentsTitleDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteContentCollectionV1ContentsCollectionDelete()`

```php
deleteContentCollectionV1ContentsCollectionDelete(): bool
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
    $result = $apiInstance->deleteContentCollectionV1ContentsCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deleteContentCollectionV1ContentsCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deletesAllContentFromCollectionV1ContentsResetCollectionDelete()`

```php
deletesAllContentFromCollectionV1ContentsResetCollectionDelete($dry_run): mixed
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
    $result = $apiInstance->deletesAllContentFromCollectionV1ContentsResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->deletesAllContentFromCollectionV1ContentsResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `gestContentByTitleV1ContentsTitleGet()`

```php
gestContentByTitleV1ContentsTitleGet($title): \OpenAPI\Client\Model\Content
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
    $result = $apiInstance->gestContentByTitleV1ContentsTitleGet($title);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->gestContentByTitleV1ContentsTitleGet: ', $e->getMessage(), PHP_EOL;
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

## `getAllContentsV1ContentsGet()`

```php
getAllContentsV1ContentsGet(): \OpenAPI\Client\Model\Content[]
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
    $result = $apiInstance->getAllContentsV1ContentsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->getAllContentsV1ContentsGet: ', $e->getMessage(), PHP_EOL;
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

## `importMultipleContentsV1ContentsPost()`

```php
importMultipleContentsV1ContentsPost($content): mixed
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
    $result = $apiInstance->importMultipleContentsV1ContentsPost($content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->importMultipleContentsV1ContentsPost: ', $e->getMessage(), PHP_EOL;
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

## `updateContentByTitleV1ContentsTitlePut()`

```php
updateContentByTitleV1ContentsTitlePut($title, $content): \OpenAPI\Client\Model\Content
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
    $result = $apiInstance->updateContentByTitleV1ContentsTitlePut($title, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->updateContentByTitleV1ContentsTitlePut: ', $e->getMessage(), PHP_EOL;
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

## `uploadFilesIntoGCSV1ContentsUploadPost()`

```php
uploadFilesIntoGCSV1ContentsUploadPost($file): object
```

Upload Files Into Gcs

Upload files into Google Storage.

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
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadFilesIntoGCSV1ContentsUploadPost($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->uploadFilesIntoGCSV1ContentsUploadPost: ', $e->getMessage(), PHP_EOL;
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
