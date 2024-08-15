# OpenAPI\Client\FaqApi

All URIs are relative to /luma, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfFAQCollectionExistsV1FaqCollectionExistsGet()**](FaqApi.md#checkIfFAQCollectionExistsV1FaqCollectionExistsGet) | **GET** /v1/faq/collection-exists | Check If Faq Collection Exists. |
| [**createFAQByQuestionV1FaqQuestionPost()**](FaqApi.md#createFAQByQuestionV1FaqQuestionPost) | **POST** /v1/faq/{question} | Create Faq By Question |
| [**createFAQCollectionV1FaqCollectionPost()**](FaqApi.md#createFAQCollectionV1FaqCollectionPost) | **POST** /v1/faq/collection | Create Faq Collection |
| [**deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete()**](FaqApi.md#deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete) | **DELETE** /v1/faq/by-internal-id/{internal_id} | Delete Faq By Internal Id |
| [**deleteFAQByQuestionV1FaqQuestionDelete()**](FaqApi.md#deleteFAQByQuestionV1FaqQuestionDelete) | **DELETE** /v1/faq/{question} | Delete Faq By Question |
| [**deleteFAQCollectionV1FaqCollectionDelete()**](FaqApi.md#deleteFAQCollectionV1FaqCollectionDelete) | **DELETE** /v1/faq/collection | Delete Faq Collection |
| [**deletesAllFAQFromCollectionV1FaqResetCollectionDelete()**](FaqApi.md#deletesAllFAQFromCollectionV1FaqResetCollectionDelete) | **DELETE** /v1/faq/reset-collection | Deletes All Faq From Collection |
| [**gestFAQByQuestionV1FaqQuestionGet()**](FaqApi.md#gestFAQByQuestionV1FaqQuestionGet) | **GET** /v1/faq/{question} | Gest Faq By Question |
| [**getAllFAQsV1FaqGet()**](FaqApi.md#getAllFAQsV1FaqGet) | **GET** /v1/faq | Get All Faqs |
| [**importMultipleFAQsV1FaqPost()**](FaqApi.md#importMultipleFAQsV1FaqPost) | **POST** /v1/faq | Import Multiple Faqs |
| [**updateFAQByQuestionV1FaqQuestionPut()**](FaqApi.md#updateFAQByQuestionV1FaqQuestionPut) | **PUT** /v1/faq/{question} | Update Faq By Question |


## `checkIfFAQCollectionExistsV1FaqCollectionExistsGet()`

```php
checkIfFAQCollectionExistsV1FaqCollectionExistsGet(): mixed
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
    $result = $apiInstance->checkIfFAQCollectionExistsV1FaqCollectionExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->checkIfFAQCollectionExistsV1FaqCollectionExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createFAQByQuestionV1FaqQuestionPost()`

```php
createFAQByQuestionV1FaqQuestionPost($question, $faq): \OpenAPI\Client\Model\Faq
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
    $result = $apiInstance->createFAQByQuestionV1FaqQuestionPost($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFAQByQuestionV1FaqQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `createFAQCollectionV1FaqCollectionPost()`

```php
createFAQCollectionV1FaqCollectionPost($delete_existing_collection): mixed
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
    $result = $apiInstance->createFAQCollectionV1FaqCollectionPost($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFAQCollectionV1FaqCollectionPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete()`

```php
deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete($internal_id): bool
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
    $result = $apiInstance->deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteFAQByQuestionV1FaqQuestionDelete()`

```php
deleteFAQByQuestionV1FaqQuestionDelete($question): bool
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
    $result = $apiInstance->deleteFAQByQuestionV1FaqQuestionDelete($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQByQuestionV1FaqQuestionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deleteFAQCollectionV1FaqCollectionDelete()`

```php
deleteFAQCollectionV1FaqCollectionDelete(): bool
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
    $result = $apiInstance->deleteFAQCollectionV1FaqCollectionDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFAQCollectionV1FaqCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `deletesAllFAQFromCollectionV1FaqResetCollectionDelete()`

```php
deletesAllFAQFromCollectionV1FaqResetCollectionDelete($dry_run): mixed
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
    $result = $apiInstance->deletesAllFAQFromCollectionV1FaqResetCollectionDelete($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deletesAllFAQFromCollectionV1FaqResetCollectionDelete: ', $e->getMessage(), PHP_EOL;
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

## `gestFAQByQuestionV1FaqQuestionGet()`

```php
gestFAQByQuestionV1FaqQuestionGet($question): \OpenAPI\Client\Model\Faq
```

Gest Faq By Question

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
    $result = $apiInstance->gestFAQByQuestionV1FaqQuestionGet($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->gestFAQByQuestionV1FaqQuestionGet: ', $e->getMessage(), PHP_EOL;
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

## `getAllFAQsV1FaqGet()`

```php
getAllFAQsV1FaqGet(): \OpenAPI\Client\Model\Faq[]
```

Get All Faqs

Returns All FAQs. If collection has a large number of FAQs, response may take long time

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
    $result = $apiInstance->getAllFAQsV1FaqGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getAllFAQsV1FaqGet: ', $e->getMessage(), PHP_EOL;
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

## `importMultipleFAQsV1FaqPost()`

```php
importMultipleFAQsV1FaqPost($faq): mixed
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
    $result = $apiInstance->importMultipleFAQsV1FaqPost($faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->importMultipleFAQsV1FaqPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **faq** | [**\OpenAPI\Client\Model\Faq[]**](../Model/Faq.md)|  | |

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

## `updateFAQByQuestionV1FaqQuestionPut()`

```php
updateFAQByQuestionV1FaqQuestionPut($question, $faq): \OpenAPI\Client\Model\Faq
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
    $result = $apiInstance->updateFAQByQuestionV1FaqQuestionPut($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->updateFAQByQuestionV1FaqQuestionPut: ', $e->getMessage(), PHP_EOL;
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
