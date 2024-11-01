# OpenAPI\Client\FaqApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfFAQCollectionExistsV1FaqsCollectionExistsGet()**](FaqApi.md#checkIfFAQCollectionExistsV1FaqsCollectionExistsGet) | **GET** /v1/faqs/collection-exists | Check If Faq Collection Exists. |
| [**createFAQByQuestionV1FaqsQuestionPost()**](FaqApi.md#createFAQByQuestionV1FaqsQuestionPost) | **POST** /v1/faqs/{question} | Create Faq By Question |
| [**createFAQCollectionV1FaqsCollectionPost()**](FaqApi.md#createFAQCollectionV1FaqsCollectionPost) | **POST** /v1/faqs/collection | Create Faq Collection |
| [**deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete()**](FaqApi.md#deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete) | **DELETE** /v1/faqs/by-internal-id/{internal_id} | Delete Faq By Internal Id |
| [**deleteFAQByQuestionV1FaqsQuestionDelete()**](FaqApi.md#deleteFAQByQuestionV1FaqsQuestionDelete) | **DELETE** /v1/faqs/{question} | Delete Faq By Question |
| [**deleteFAQCollectionV1FaqsCollectionDelete()**](FaqApi.md#deleteFAQCollectionV1FaqsCollectionDelete) | **DELETE** /v1/faqs/collection | Delete Faq Collection |
| [**deletesAllFAQFromCollectionV1FaqsResetCollectionDelete()**](FaqApi.md#deletesAllFAQFromCollectionV1FaqsResetCollectionDelete) | **DELETE** /v1/faqs/reset-collection | Deletes All Faq From Collection |
| [**getAllFAQsV1FaqsGet()**](FaqApi.md#getAllFAQsV1FaqsGet) | **GET** /v1/faqs | Get All Faqs |
| [**getFAQByQuestionV1FaqsQuestionGet()**](FaqApi.md#getFAQByQuestionV1FaqsQuestionGet) | **GET** /v1/faqs/{question} | Get Faq By Question |
| [**importMultipleFAQsV1FaqsPost()**](FaqApi.md#importMultipleFAQsV1FaqsPost) | **POST** /v1/faqs | Import Multiple Faqs |
| [**updateFAQByQuestionV1FaqsQuestionPut()**](FaqApi.md#updateFAQByQuestionV1FaqsQuestionPut) | **PUT** /v1/faqs/{question} | Update Faq By Question |
| [**uploadFilesIntoGCSV1FaqsUploadPost()**](FaqApi.md#uploadFilesIntoGCSV1FaqsUploadPost) | **POST** /v1/faqs/upload | Upload Files Into Gcs |


## `checkIfFAQCollectionExistsV1FaqsCollectionExistsGet()`

```php
checkIfFAQCollectionExistsV1FaqsCollectionExistsGet(): mixed
```

Check If Faq Collection Exists.

Returns true if FAQ collection exists else return false

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->checkIfFAQCollectionExistsV1FaqsCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->checkIfFAQCollectionExistsV1FaqsCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createFAQByQuestionV1FaqsQuestionPost()`

```php
createFAQByQuestionV1FaqsQuestionPost($question, $faq): \OpenAPI\Client\Model\Faq
```

Create Faq By Question

Create FAQ by question

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$question = 'question_example'; // string
$faq = new \OpenAPI\Client\Model\Faq(); // \OpenAPI\Client\Model\Faq

try {
    $result = $apiInstance->createFAQByQuestionV1FaqsQuestionPost($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFAQByQuestionV1FaqsQuestionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **question** | **string**|  | |
| **faq** | [**\OpenAPI\Client\Model\Faq**](../Model/Faq.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Faq**](../Model/Faq.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createFAQCollectionV1FaqsCollectionPost()`

```php
createFAQCollectionV1FaqsCollectionPost($delete_existing_collection): mixed
```

Create Faq Collection

Creates FAQ collection/schema in Weaviate database

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delete_existing_collection = false; // bool

try {
    $result = $apiInstance->createFAQCollectionV1FaqsCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFAQCollectionV1FaqsCollectionPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete()`

```php
deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete($internal_id): bool
```

Delete Faq By Internal Id

Delete FAQ by internal_id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$internal_id = 56; // int

try {
    $result = $apiInstance->deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQByInternalIdV1FaqsByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteFAQByQuestionV1FaqsQuestionDelete()`

```php
deleteFAQByQuestionV1FaqsQuestionDelete($question): bool
```

Delete Faq By Question

Delete FAQ by question

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$question = 'question_example'; // string

try {
    $result = $apiInstance->deleteFAQByQuestionV1FaqsQuestionDelete($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQByQuestionV1FaqsQuestionDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **question** | **string**|  | |

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

## `deleteFAQCollectionV1FaqsCollectionDelete()`

```php
deleteFAQCollectionV1FaqsCollectionDelete(): bool
```

Delete Faq Collection

Delete FAQ collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteFAQCollectionV1FaqsCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQCollectionV1FaqsCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deletesAllFAQFromCollectionV1FaqsResetCollectionDelete()`

```php
deletesAllFAQFromCollectionV1FaqsResetCollectionDelete($dry_run): mixed
```

Deletes All Faq From Collection

Deletes all FAQ from collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dry_run = true; // bool

try {
    $result = $apiInstance->deletesAllFAQFromCollectionV1FaqsResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deletesAllFAQFromCollectionV1FaqsResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `getAllFAQsV1FaqsGet()`

```php
getAllFAQsV1FaqsGet(): \OpenAPI\Client\Model\Faq[]
```

Get All Faqs

Returns All FAQs. If collection has a large number of FAQs                 response may take long time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllFAQsV1FaqsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getAllFAQsV1FaqsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Faq[]**](../Model/Faq.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFAQByQuestionV1FaqsQuestionGet()`

```php
getFAQByQuestionV1FaqsQuestionGet($question): \OpenAPI\Client\Model\Faq
```

Get Faq By Question

Get FAQ by question

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$question = 'question_example'; // string

try {
    $result = $apiInstance->getFAQByQuestionV1FaqsQuestionGet($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getFAQByQuestionV1FaqsQuestionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **question** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Faq**](../Model/Faq.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `importMultipleFAQsV1FaqsPost()`

```php
importMultipleFAQsV1FaqsPost($faq): \OpenAPI\Client\Model\Faq[]
```

Import Multiple Faqs

Import multiple FAQs. If a FAQ same question already exist, it is updated. Otherwise new FAQ is created

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$faq = array(new \OpenAPI\Client\Model\Faq()); // \OpenAPI\Client\Model\Faq[]

try {
    $result = $apiInstance->importMultipleFAQsV1FaqsPost($faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->importMultipleFAQsV1FaqsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **faq** | [**\OpenAPI\Client\Model\Faq[]**](../Model/Faq.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Faq[]**](../Model/Faq.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateFAQByQuestionV1FaqsQuestionPut()`

```php
updateFAQByQuestionV1FaqsQuestionPut($question, $faq): \OpenAPI\Client\Model\Faq
```

Update Faq By Question

Update FAQ By question

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$question = 'question_example'; // string
$faq = new \OpenAPI\Client\Model\Faq(); // \OpenAPI\Client\Model\Faq

try {
    $result = $apiInstance->updateFAQByQuestionV1FaqsQuestionPut($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->updateFAQByQuestionV1FaqsQuestionPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **question** | **string**|  | |
| **faq** | [**\OpenAPI\Client\Model\Faq**](../Model/Faq.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Faq**](../Model/Faq.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadFilesIntoGCSV1FaqsUploadPost()`

```php
uploadFilesIntoGCSV1FaqsUploadPost($file): object
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


$apiInstance = new OpenAPI\Client\Api\FaqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadFilesIntoGCSV1FaqsUploadPost($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->uploadFilesIntoGCSV1FaqsUploadPost: ', $e->getMessage(), PHP_EOL;
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
