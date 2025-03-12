# OpenAPI\Client\SchemaApi

All URIs are relative to /tenant, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet()**](SchemaApi.md#checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet) | **GET** /v1/schema/is-schema-exists | Check If Tenant Schema Exists. |
| [**createTenantSchemaAndRequireTablesV1SchemaSchemaPost()**](SchemaApi.md#createTenantSchemaAndRequireTablesV1SchemaSchemaPost) | **POST** /v1/schema/schema | Create Tenant Schema And Require Tables |


## `checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet()`

```php
checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet(): mixed
```

Check If Tenant Schema Exists.

Returns true if tenant schema exists else return false

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SchemaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SchemaApi->checkIfTenantSchemaExistsV1SchemaIsSchemaExistsGet: ', $e->getMessage(), PHP_EOL;
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

## `createTenantSchemaAndRequireTablesV1SchemaSchemaPost()`

```php
createTenantSchemaAndRequireTablesV1SchemaSchemaPost(): mixed
```

Create Tenant Schema And Require Tables

Create Tenant Schema And Require Tables: config, llm_prompt

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SchemaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->createTenantSchemaAndRequireTablesV1SchemaSchemaPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SchemaApi->createTenantSchemaAndRequireTablesV1SchemaSchemaPost: ', $e->getMessage(), PHP_EOL;
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
