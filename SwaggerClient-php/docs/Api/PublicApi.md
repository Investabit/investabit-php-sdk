# Swagger\Client\PublicApi

All URIs are relative to *https://api.cryptoweather.ai*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1PublicPriceChangeSymbolGet**](PublicApi.md#v1PublicPriceChangeSymbolGet) | **GET** /v1/public/price-change/{symbol} | Price Change
[**v1PublicPriceCurrentSymbolGet**](PublicApi.md#v1PublicPriceCurrentSymbolGet) | **GET** /v1/public/price-current/{symbol} | Price Current
[**v1PublicPriceHistorySymbolPeriodIntervalGet**](PublicApi.md#v1PublicPriceHistorySymbolPeriodIntervalGet) | **GET** /v1/public/price-history/{symbol}/{period}/{interval} | Price History
[**v1PublicSymbolsGet**](PublicApi.md#v1PublicSymbolsGet) | **GET** /v1/public/symbols | Symbols
[**v1PublicTrendSymbolGet**](PublicApi.md#v1PublicTrendSymbolGet) | **GET** /v1/public/trend/{symbol} | Trend


# **v1PublicPriceChangeSymbolGet**
> \Swagger\Client\Model\PublicPriceChangeResponse v1PublicPriceChangeSymbolGet($symbol)

Price Change



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "btc"; // string | The cryptocurrency symbol.

try {
    $result = $apiInstance->v1PublicPriceChangeSymbolGet($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicPriceChangeSymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol. |

### Return type

[**\Swagger\Client\Model\PublicPriceChangeResponse**](../Model/PublicPriceChangeResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PublicPriceCurrentSymbolGet**
> \Swagger\Client\Model\PublicPriceCurrentResponse v1PublicPriceCurrentSymbolGet($symbol)

Price Current



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "btc"; // string | The cryptocurrency symbol, provide `all` to get every symbol.

try {
    $result = $apiInstance->v1PublicPriceCurrentSymbolGet($symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicPriceCurrentSymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol, provide &#x60;all&#x60; to get every symbol. |

### Return type

[**\Swagger\Client\Model\PublicPriceCurrentResponse**](../Model/PublicPriceCurrentResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PublicPriceHistorySymbolPeriodIntervalGet**
> \Swagger\Client\Model\PublicPriceHistoryResponse v1PublicPriceHistorySymbolPeriodIntervalGet($symbol, $period, $interval)

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
$symbol = "btc"; // string | The cryptocurrency symbol, provide `all` to get every symbol.
$period = "30d"; // string | The period to get data for, such as past 30 days.
$interval = "1d"; // string | The bar interval, such as 1 day.

try {
    $result = $apiInstance->v1PublicPriceHistorySymbolPeriodIntervalGet($symbol, $period, $interval);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicApi->v1PublicPriceHistorySymbolPeriodIntervalGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol, provide &#x60;all&#x60; to get every symbol. |
 **period** | **string**| The period to get data for, such as past 30 days. |
 **interval** | **string**| The bar interval, such as 1 day. |

### Return type

[**\Swagger\Client\Model\PublicPriceHistoryResponse**](../Model/PublicPriceHistoryResponse.md)

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

The trend response contains a collection of forecasts for different intervals with the following attributes.  + `time_start` start time of the period the forecast is applicable for  + `time_end` end time of the period the forecast is applicable for  + `interval` interval in hours that the forecast is applicable for  + `weighted_price` forecasted weighted price during the period  + `change_pct` percent change in price for forecasted weighted_price relative to current price  + `change_usd` dollar change in price for forecasted weighted_price relative to current price

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PublicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$symbol = "btc"; // string | The cryptocurrency symbol.

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
 **symbol** | **string**| The cryptocurrency symbol. |

### Return type

[**\Swagger\Client\Model\PublicTrendResponse**](../Model/PublicTrendResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

