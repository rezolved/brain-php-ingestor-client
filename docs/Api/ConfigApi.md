# OpenAPI\Client\ConfigApi

All URIs are relative to /tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete()**](ConfigApi.md#deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete) | **DELETE** /v1/config/config-by-key | Delete Data By Key From &#39;Config&#39; Table. |
| [**getAllDataFromConfigTableV1ConfigConfigGetAllGet()**](ConfigApi.md#getAllDataFromConfigTableV1ConfigConfigGetAllGet) | **GET** /v1/config/config-get-all | Get All Data From Config Table. |
| [**getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet()**](ConfigApi.md#getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet) | **GET** /v1/config/config-get-by-key | Get Data By Key From Config Table. |
| [**insertDataToConfigTableV1ConfigConfigPost()**](ConfigApi.md#insertDataToConfigTableV1ConfigConfigPost) | **POST** /v1/config/config | Insert Data To Config Table. |


## `deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete()`

```php
deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete($key): mixed
```

Delete Data By Key From 'Config' Table.

Delete data by key from 'config' table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ConfigApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string

try {
    $result = $apiInstance->deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete($key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigApi->deleteDataByKeyFromConfigTableV1ConfigConfigByKeyDelete: ', $e->getMessage(), PHP_EOL;
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

## `getAllDataFromConfigTableV1ConfigConfigGetAllGet()`

```php
getAllDataFromConfigTableV1ConfigConfigGetAllGet(): mixed
```

Get All Data From Config Table.

Get all data from config table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ConfigApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllDataFromConfigTableV1ConfigConfigGetAllGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigApi->getAllDataFromConfigTableV1ConfigConfigGetAllGet: ', $e->getMessage(), PHP_EOL;
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

## `getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet()`

```php
getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet($key): mixed
```

Get Data By Key From Config Table.

Get data by key from config table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ConfigApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string

try {
    $result = $apiInstance->getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet($key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigApi->getDataByKeyFromConfigTableV1ConfigConfigGetByKeyGet: ', $e->getMessage(), PHP_EOL;
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

## `insertDataToConfigTableV1ConfigConfigPost()`

```php
insertDataToConfigTableV1ConfigConfigPost($config_model): mixed
```

Insert Data To Config Table.

Insert data to config table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ConfigApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$config_model = new \OpenAPI\Client\Model\ConfigModel(); // \OpenAPI\Client\Model\ConfigModel

try {
    $result = $apiInstance->insertDataToConfigTableV1ConfigConfigPost($config_model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigApi->insertDataToConfigTableV1ConfigConfigPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **config_model** | [**\OpenAPI\Client\Model\ConfigModel**](../Model/ConfigModel.md)|  | |

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
