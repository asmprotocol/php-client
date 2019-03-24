# SwaggerClient-php
Application Server Management Protocol server

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
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
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\Check(); // \ASMP\Client\Model\Check | Check request

try {
    $apiInstance->check($body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->check: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\Request(); // \ASMP\Client\Model\Request | Request request

try {
    $apiInstance->request($body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->request: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | UUID of the request to get the status from

try {
    $apiInstance->status($id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->status: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://swagger.asmp.io/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**check**](docs/Api/DefaultApi.md#check) | **POST** /check | Check for potential changes
*DefaultApi* | [**request**](docs/Api/DefaultApi.md#request) | **POST** /request | Request a specific change
*DefaultApi* | [**status**](docs/Api/DefaultApi.md#status) | **GET** /status/{id} | Get the current status for a given request ID

## Documentation For Models

 - [Change](docs/Model/Change.md)
 - [Check](docs/Model/Check.md)
 - [CheckResponse](docs/Model/CheckResponse.md)
 - [Component](docs/Model/Component.md)
 - [ComponentGroup](docs/Model/ComponentGroup.md)
 - [Constraint](docs/Model/Constraint.md)
 - [Request](docs/Model/Request.md)
 - [RequestResponse](docs/Model/RequestResponse.md)
 - [RollbackId](docs/Model/RollbackId.md)
 - [StatusResponse](docs/Model/StatusResponse.md)

## Documentation For Authorization


## asmp_auth

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header


## Author

apiteam@asmp.io
