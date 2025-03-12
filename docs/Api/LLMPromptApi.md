# OpenAPI\Client\LLMPromptApi

All URIs are relative to /tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete()**](LLMPromptApi.md#deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete) | **DELETE** /v1/tenant/llm-prompt-by-key | Delete Data By Key From &#39;Llm Prompt&#39; Table. |
| [**getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet()**](LLMPromptApi.md#getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet) | **GET** /v1/tenant/llm-prompt-get-all | Get All Data From &#39;Llm-Prompt&#39; Table. |
| [**getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet()**](LLMPromptApi.md#getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet) | **GET** /v1/tenant/llm-prompt-get-by-key | Get Data By Key From &#39;Llm-Prompt&#39; Table. |
| [**insertDataToLlmPromptTableV1TenantLlmPromptPost()**](LLMPromptApi.md#insertDataToLlmPromptTableV1TenantLlmPromptPost) | **POST** /v1/tenant/llm-prompt | Insert Data To &#39;Llm-Prompt&#39; Table. |


## `deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete()`

```php
deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete($key): mixed
```

Delete Data By Key From 'Llm Prompt' Table.

Delete data by key from 'llm_prompt' table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\LLMPromptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string

try {
    $result = $apiInstance->deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete($key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LLMPromptApi->deleteDataByKeyFromLlmPromptTableV1TenantLlmPromptByKeyDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **key** | **string**|  | |

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

## `getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet()`

```php
getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet(): mixed
```

Get All Data From 'Llm-Prompt' Table.

Get all data from 'llm-prompt' table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\LLMPromptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LLMPromptApi->getAllDataFromLlmPromptTableV1TenantLlmPromptGetAllGet: ', $e->getMessage(), PHP_EOL;
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

## `getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet()`

```php
getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet($key): mixed
```

Get Data By Key From 'Llm-Prompt' Table.

Get data by key from 'llm-prompt' table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\LLMPromptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string

try {
    $result = $apiInstance->getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet($key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LLMPromptApi->getDataByKeyFromLlmPromptTableV1TenantLlmPromptGetByKeyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **key** | **string**|  | |

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

## `insertDataToLlmPromptTableV1TenantLlmPromptPost()`

```php
insertDataToLlmPromptTableV1TenantLlmPromptPost($llm_prompt_model): mixed
```

Insert Data To 'Llm-Prompt' Table.

Insert data to 'llm-prompt' table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\LLMPromptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$llm_prompt_model = new \OpenAPI\Client\Model\LlmPromptModel(); // \OpenAPI\Client\Model\LlmPromptModel

try {
    $result = $apiInstance->insertDataToLlmPromptTableV1TenantLlmPromptPost($llm_prompt_model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LLMPromptApi->insertDataToLlmPromptTableV1TenantLlmPromptPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **llm_prompt_model** | [**\OpenAPI\Client\Model\LlmPromptModel**](../Model/LlmPromptModel.md)|  | |

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
