# Swagger\Client\PublicApi

All URIs are relative to *https://api.investabit.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1PublicCurrentSymbolGet**](PublicApi.md#v1PublicCurrentSymbolGet) | **GET** /v1/public/current/{symbol} | Current
[**v1PublicPriceHistorySymbolGet**](PublicApi.md#v1PublicPriceHistorySymbolGet) | **GET** /v1/public/price-history/{symbol} | Price History
[**v1PublicSymbolsGet**](PublicApi.md#v1PublicSymbolsGet) | **GET** /v1/public/symbols | Symbols
[**v1PublicTrendSymbolGet**](PublicApi.md#v1PublicTrendSymbolGet) | **GET** /v1/public/trend/{symbol} | Trend


# **v1PublicCurrentSymbolGet**
> \Swagger\Client\Model\PublicCurrentResponse v1PublicCurrentSymbolGet($symbol)

Current



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "\"btc\""; // string | The cryptocurrency symbol, default is btc.

try {
    $result = $apiInstance->v1PublicCurrentSymbolGet($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicCurrentSymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol, default is btc. |

### Return type

[**\Swagger\Client\Model\PublicCurrentResponse**](../Model/PublicCurrentResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PublicPriceHistorySymbolGet**
> \Swagger\Client\Model\PublicPriceResponse v1PublicPriceHistorySymbolGet($symbol)

Price History



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "\"btc\""; // string | The cryptocurrency symbol, default is btc.

try {
    $result = $apiInstance->v1PublicPriceHistorySymbolGet($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicPriceHistorySymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol, default is btc. |

### Return type

[**\Swagger\Client\Model\PublicPriceResponse**](../Model/PublicPriceResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PublicSymbolsGet**
> \Swagger\Client\Model\PublicSymbolsResponse v1PublicSymbolsGet()

Symbols



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->v1PublicSymbolsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicSymbolsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\PublicSymbolsResponse**](../Model/PublicSymbolsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PublicTrendSymbolGet**
> \Swagger\Client\Model\PublicTrendResponse v1PublicTrendSymbolGet($symbol)

Trend



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "\"btc\""; // string | The cryptocurrency symbol, default is btc.

try {
    $result = $apiInstance->v1PublicTrendSymbolGet($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicTrendSymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol, default is btc. |

### Return type

[**\Swagger\Client\Model\PublicTrendResponse**](../Model/PublicTrendResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

