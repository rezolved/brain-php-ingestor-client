# OpenAPI\Client\FaqApi

All URIs are relative to /tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createFaqByQuestion()**](FaqApi.md#createFaqByQuestion) | **POST** /v1/faq/{question} | Create Faq By Question |
| [**createFaqCollection()**](FaqApi.md#createFaqCollection) | **POST** /v1/faq/collection | Create Faq Collection |
| [**deleteFaqByInternalId()**](FaqApi.md#deleteFaqByInternalId) | **DELETE** /v1/faq/by-internal-id/{internal_id} | Delete Faq By Internal Id |
| [**deleteFaqByQuestion()**](FaqApi.md#deleteFaqByQuestion) | **DELETE** /v1/faq/{question} | Delete Faq By Question |
| [**deleteFaqCollection()**](FaqApi.md#deleteFaqCollection) | **DELETE** /v1/faq/collection | Delete Faq Collection |
| [**getAllFaqs()**](FaqApi.md#getAllFaqs) | **GET** /v1/faq | Get All Faqs |
| [**getFaqByQuestion()**](FaqApi.md#getFaqByQuestion) | **GET** /v1/faq/{question} | Get Faq By Question |
| [**getFaqCollectionExists()**](FaqApi.md#getFaqCollectionExists) | **GET** /v1/faq/collection-exists | Check If Faq Collection Exists. |
| [**importMultipleFaqs()**](FaqApi.md#importMultipleFaqs) | **POST** /v1/faq | Import Multiple Faqs |
| [**resetFaqCollection()**](FaqApi.md#resetFaqCollection) | **DELETE** /v1/faq/reset-collection | Deletes All Faq From Collection |
| [**updateFaqByQuestion()**](FaqApi.md#updateFaqByQuestion) | **PUT** /v1/faq/{question} | Update Faq By Question |


## `createFaqByQuestion()`

```php
createFaqByQuestion($question, $faq): \OpenAPI\Client\Model\Faq
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
    $result = $apiInstance->createFaqByQuestion($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFaqByQuestion: ', $e->getMessage(), PHP_EOL;
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

## `createFaqCollection()`

```php
createFaqCollection($delete_existing_collection): mixed
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
    $result = $apiInstance->createFaqCollection($delete_existing_collection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->createFaqCollection: ', $e->getMessage(), PHP_EOL;
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

## `deleteFaqByInternalId()`

```php
deleteFaqByInternalId($internal_id): bool
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
    $result = $apiInstance->deleteFaqByInternalId($internal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFaqByInternalId: ', $e->getMessage(), PHP_EOL;
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

## `deleteFaqByQuestion()`

```php
deleteFaqByQuestion($question): bool
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
    $result = $apiInstance->deleteFaqByQuestion($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFaqByQuestion: ', $e->getMessage(), PHP_EOL;
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

## `deleteFaqCollection()`

```php
deleteFaqCollection(): bool
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
    $result = $apiInstance->deleteFaqCollection();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->deleteFaqCollection: ', $e->getMessage(), PHP_EOL;
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

## `getAllFaqs()`

```php
getAllFaqs(): \OpenAPI\Client\Model\Faq[]
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
    $result = $apiInstance->getAllFaqs();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getAllFaqs: ', $e->getMessage(), PHP_EOL;
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

## `getFaqByQuestion()`

```php
getFaqByQuestion($question): \OpenAPI\Client\Model\Faq
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
    $result = $apiInstance->getFaqByQuestion($question);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getFaqByQuestion: ', $e->getMessage(), PHP_EOL;
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

## `getFaqCollectionExists()`

```php
getFaqCollectionExists(): mixed
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
    $result = $apiInstance->getFaqCollectionExists();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->getFaqCollectionExists: ', $e->getMessage(), PHP_EOL;
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

## `importMultipleFaqs()`

```php
importMultipleFaqs($faq): \OpenAPI\Client\Model\Faq[]
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
    $result = $apiInstance->importMultipleFaqs($faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->importMultipleFaqs: ', $e->getMessage(), PHP_EOL;
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

## `resetFaqCollection()`

```php
resetFaqCollection($dry_run): mixed
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
    $result = $apiInstance->resetFaqCollection($dry_run);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->resetFaqCollection: ', $e->getMessage(), PHP_EOL;
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

## `updateFaqByQuestion()`

```php
updateFaqByQuestion($question, $faq): \OpenAPI\Client\Model\Faq
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
    $result = $apiInstance->updateFaqByQuestion($question, $faq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FaqApi->updateFaqByQuestion: ', $e->getMessage(), PHP_EOL;
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
