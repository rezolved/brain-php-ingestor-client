# OpenAPIClient-php

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to */luma*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ContentApi* | [**checkIfContentCollectionExistsV1ContentCollectionExistsGet**](docs/Api/ContentApi.md#checkifcontentcollectionexistsv1contentcollectionexistsget) | **GET** /v1/content/collection-exists | Check If Content Collection Exists.
*ContentApi* | [**createContentByTitleV1ContentTitlePost**](docs/Api/ContentApi.md#createcontentbytitlev1contenttitlepost) | **POST** /v1/content/{title} | Create Content By Title
*ContentApi* | [**createContentCollectionV1ContentCollectionPost**](docs/Api/ContentApi.md#createcontentcollectionv1contentcollectionpost) | **POST** /v1/content/collection | Create Content Collection
*ContentApi* | [**deleteContentByInternalIdV1ContentByInternalIdInternalIdDelete**](docs/Api/ContentApi.md#deletecontentbyinternalidv1contentbyinternalidinternaliddelete) | **DELETE** /v1/content/by-internal-id/{internal_id} | Delete Content By Internal Id
*ContentApi* | [**deleteContentByTitleV1ContentTitleDelete**](docs/Api/ContentApi.md#deletecontentbytitlev1contenttitledelete) | **DELETE** /v1/content/{title} | Delete Content By Title
*ContentApi* | [**deleteContentCollectionV1ContentCollectionDelete**](docs/Api/ContentApi.md#deletecontentcollectionv1contentcollectiondelete) | **DELETE** /v1/content/collection | Delete Content Collection
*ContentApi* | [**deletesAllContentFromCollectionV1ContentResetCollectionDelete**](docs/Api/ContentApi.md#deletesallcontentfromcollectionv1contentresetcollectiondelete) | **DELETE** /v1/content/reset-collection | Deletes All Content From Collection
*ContentApi* | [**gestContentByTitleV1ContentTitleGet**](docs/Api/ContentApi.md#gestcontentbytitlev1contenttitleget) | **GET** /v1/content/{title} | Gest Content By Title
*ContentApi* | [**getAllContentsV1ContentGet**](docs/Api/ContentApi.md#getallcontentsv1contentget) | **GET** /v1/content | Get All Contents
*ContentApi* | [**importMultipleContentsV1ContentPost**](docs/Api/ContentApi.md#importmultiplecontentsv1contentpost) | **POST** /v1/content | Import Multiple Contents
*ContentApi* | [**updateContentByTitleV1ContentTitlePut**](docs/Api/ContentApi.md#updatecontentbytitlev1contenttitleput) | **PUT** /v1/content/{title} | Update Content By Title
*DefaultApi* | [**healthCheckV1HealthGet**](docs/Api/DefaultApi.md#healthcheckv1healthget) | **GET** /v1/health | Health Check
*FaqApi* | [**checkIfFAQCollectionExistsV1FaqCollectionExistsGet**](docs/Api/FaqApi.md#checkiffaqcollectionexistsv1faqcollectionexistsget) | **GET** /v1/faq/collection-exists | Check If Faq Collection Exists.
*FaqApi* | [**createFAQByQuestionV1FaqQuestionPost**](docs/Api/FaqApi.md#createfaqbyquestionv1faqquestionpost) | **POST** /v1/faq/{question} | Create Faq By Question
*FaqApi* | [**createFAQCollectionV1FaqCollectionPost**](docs/Api/FaqApi.md#createfaqcollectionv1faqcollectionpost) | **POST** /v1/faq/collection | Create Faq Collection
*FaqApi* | [**deleteFAQByInternalIdV1FaqByInternalIdInternalIdDelete**](docs/Api/FaqApi.md#deletefaqbyinternalidv1faqbyinternalidinternaliddelete) | **DELETE** /v1/faq/by-internal-id/{internal_id} | Delete Faq By Internal Id
*FaqApi* | [**deleteFAQByQuestionV1FaqQuestionDelete**](docs/Api/FaqApi.md#deletefaqbyquestionv1faqquestiondelete) | **DELETE** /v1/faq/{question} | Delete Faq By Question
*FaqApi* | [**deleteFAQCollectionV1FaqCollectionDelete**](docs/Api/FaqApi.md#deletefaqcollectionv1faqcollectiondelete) | **DELETE** /v1/faq/collection | Delete Faq Collection
*FaqApi* | [**deletesAllFAQFromCollectionV1FaqResetCollectionDelete**](docs/Api/FaqApi.md#deletesallfaqfromcollectionv1faqresetcollectiondelete) | **DELETE** /v1/faq/reset-collection | Deletes All Faq From Collection
*FaqApi* | [**gestFAQByQuestionV1FaqQuestionGet**](docs/Api/FaqApi.md#gestfaqbyquestionv1faqquestionget) | **GET** /v1/faq/{question} | Gest Faq By Question
*FaqApi* | [**getAllFAQsV1FaqGet**](docs/Api/FaqApi.md#getallfaqsv1faqget) | **GET** /v1/faq | Get All Faqs
*FaqApi* | [**importMultipleFAQsV1FaqPost**](docs/Api/FaqApi.md#importmultiplefaqsv1faqpost) | **POST** /v1/faq | Import Multiple Faqs
*FaqApi* | [**updateFAQByQuestionV1FaqQuestionPut**](docs/Api/FaqApi.md#updatefaqbyquestionv1faqquestionput) | **PUT** /v1/faq/{question} | Update Faq By Question
*ProductApi* | [**checkIfProductCollectionExistsV1ProductCollectionExistsGet**](docs/Api/ProductApi.md#checkifproductcollectionexistsv1productcollectionexistsget) | **GET** /v1/product/collection-exists | Check If Product Collection Exists.
*ProductApi* | [**createProductBySKUV1ProductSkuPost**](docs/Api/ProductApi.md#createproductbyskuv1productskupost) | **POST** /v1/product/{sku} | Create Product By Sku
*ProductApi* | [**createProductCollectionV1ProductCollectionPost**](docs/Api/ProductApi.md#createproductcollectionv1productcollectionpost) | **POST** /v1/product/collection | Create Product Collection
*ProductApi* | [**deleteProductByInternalIdV1ProductByInternalIdInternalIdDelete**](docs/Api/ProductApi.md#deleteproductbyinternalidv1productbyinternalidinternaliddelete) | **DELETE** /v1/product/by-internal-id/{internal_id} | Delete Product By Internal Id
*ProductApi* | [**deleteProductBySKUV1ProductSkuDelete**](docs/Api/ProductApi.md#deleteproductbyskuv1productskudelete) | **DELETE** /v1/product/{sku} | Delete Product By Sku
*ProductApi* | [**deleteProductCollectionV1ProductCollectionDelete**](docs/Api/ProductApi.md#deleteproductcollectionv1productcollectiondelete) | **DELETE** /v1/product/collection | Delete Product Collection
*ProductApi* | [**deletesAllProductsFromCollectionV1ProductResetCollectionDelete**](docs/Api/ProductApi.md#deletesallproductsfromcollectionv1productresetcollectiondelete) | **DELETE** /v1/product/reset-collection | Deletes All Products From Collection
*ProductApi* | [**gestProductBySKUV1ProductSkuGet**](docs/Api/ProductApi.md#gestproductbyskuv1productskuget) | **GET** /v1/product/{sku} | Gest Product By Sku
*ProductApi* | [**getAllProductsV1ProductGet**](docs/Api/ProductApi.md#getallproductsv1productget) | **GET** /v1/product | Get All Products
*ProductApi* | [**importMultipleProductsV1ProductPost**](docs/Api/ProductApi.md#importmultipleproductsv1productpost) | **POST** /v1/product | Import Multiple Products
*ProductApi* | [**updateProductBySKUV1ProductSkuPut**](docs/Api/ProductApi.md#updateproductbyskuv1productskuput) | **PUT** /v1/product/{sku} | Update Product By Sku

## Models

- [Content](docs/Model/Content.md)
- [Faq](docs/Model/Faq.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [Product](docs/Model/Product.md)
- [ProductAvailability](docs/Model/ProductAvailability.md)
- [ValidationError](docs/Model/ValidationError.md)
- [ValidationErrorLocInner](docs/Model/ValidationErrorLocInner.md)

## Authorization

Authentication schemes defined for the API:
### APIKeyHeader

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `0.2.0`
    - Generator version: `7.7.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
