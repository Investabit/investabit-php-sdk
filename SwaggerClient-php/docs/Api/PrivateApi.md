# Swagger\Client\PrivateApi

All URIs are relative to *https://api.cryptoweather.ai*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1PrivateAccuracySymbolIntervalPeriodGet**](PrivateApi.md#v1PrivateAccuracySymbolIntervalPeriodGet) | **GET** /v1/private/accuracy/{symbol}/{interval}/{period} | Accuracy
[**v1PrivateForecastSymbolIntervalGet**](PrivateApi.md#v1PrivateForecastSymbolIntervalGet) | **GET** /v1/private/forecast/{symbol}/{interval} | Forecast
[**v1PrivateForecastTimeSymbolIntervalPeriodGet**](PrivateApi.md#v1PrivateForecastTimeSymbolIntervalPeriodGet) | **GET** /v1/private/forecast-time/{symbol}/{interval}/{period} | Forecast Time
[**v1PrivateTrendSymbolGet**](PrivateApi.md#v1PrivateTrendSymbolGet) | **GET** /v1/private/trend/{symbol} | Trend
[**v1PrivateTrendTabularGet**](PrivateApi.md#v1PrivateTrendTabularGet) | **GET** /v1/private/trend-tabular | Trend Tabular


# **v1PrivateAccuracySymbolIntervalPeriodGet**
> \Swagger\Client\Model\PrivateAccuracyResponse v1PrivateAccuracySymbolIntervalPeriodGet($symbol, $interval, $period, $cookie, $x_csrf)

Accuracy

The accuracy response contains the following attributes.  + `rmse` Root Mean Square Error  + `mae` Mean Absolute error  + `r2` R Squared  + `ci` Confidence Interval lower and upper error bounds

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: oauth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PrivateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = "btc"; // string | The cryptocurrency symbol.
$interval = "1h"; // string | The forecast interval, 1h or 1d.
$period = "7d"; // string | The period for computing the accuracy, such as the past 7 days.
$cookie = "csrf=b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. csrf=b1820141-1bad-4a9c-93c0-52022817ce89
$x_csrf = "b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. b1820141-1bad-4a9c-93c0-52022817ce89

try {
    $result = $apiInstance->v1PrivateAccuracySymbolIntervalPeriodGet($symbol, $interval, $period, $cookie, $x_csrf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateApi->v1PrivateAccuracySymbolIntervalPeriodGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol. |
 **interval** | **string**| The forecast interval, 1h or 1d. |
 **period** | **string**| The period for computing the accuracy, such as the past 7 days. |
 **cookie** | **string**| e.g. csrf&#x3D;b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]
 **x_csrf** | **string**| e.g. b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]

### Return type

[**\Swagger\Client\Model\PrivateAccuracyResponse**](../Model/PrivateAccuracyResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PrivateForecastSymbolIntervalGet**
> \Swagger\Client\Model\PrivateForecastResponse v1PrivateForecastSymbolIntervalGet($symbol, $interval, $cookie, $x_csrf)

Forecast

The forecast response contains a sequence of forecasts at the specified intervals, with the following attributes.  + `time_start` start time of the period the forecast is applicable for  + `time_end` end time of the period the forecast is applicable for  + `low` forecasted high during the period  + `high` forecasted low during the period  + `weighted_price` forecasted weighted price during the period  + `change_pct` percent change in price for forecasted weighted_price relative to current price  + `change_usd` dollar change in price for forecasted weighted_price relative to current price

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: oauth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PrivateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = "btc"; // string | The cryptocurrency symbol.
$interval = "1h"; // string | The forecast interval, 1h or 1d.
$cookie = "csrf=b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. csrf=b1820141-1bad-4a9c-93c0-52022817ce89
$x_csrf = "b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. b1820141-1bad-4a9c-93c0-52022817ce89

try {
    $result = $apiInstance->v1PrivateForecastSymbolIntervalGet($symbol, $interval, $cookie, $x_csrf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateApi->v1PrivateForecastSymbolIntervalGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol. |
 **interval** | **string**| The forecast interval, 1h or 1d. |
 **cookie** | **string**| e.g. csrf&#x3D;b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]
 **x_csrf** | **string**| e.g. b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]

### Return type

[**\Swagger\Client\Model\PrivateForecastResponse**](../Model/PrivateForecastResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PrivateForecastTimeSymbolIntervalPeriodGet**
> \Swagger\Client\Model\PrivateForecastTimeResponse v1PrivateForecastTimeSymbolIntervalPeriodGet($symbol, $interval, $period, $cookie, $x_csrf)

Forecast Time



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: oauth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PrivateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = "btc"; // string | The cryptocurrency symbol.
$interval = "1h"; // string | The forecast interval, 1h or 1d.
$period = "7d"; // string | The period for computing the error bounds, typically 7d or 30d.
$cookie = "csrf=b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. csrf=b1820141-1bad-4a9c-93c0-52022817ce89
$x_csrf = "b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. b1820141-1bad-4a9c-93c0-52022817ce89

try {
    $result = $apiInstance->v1PrivateForecastTimeSymbolIntervalPeriodGet($symbol, $interval, $period, $cookie, $x_csrf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateApi->v1PrivateForecastTimeSymbolIntervalPeriodGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol. |
 **interval** | **string**| The forecast interval, 1h or 1d. |
 **period** | **string**| The period for computing the error bounds, typically 7d or 30d. |
 **cookie** | **string**| e.g. csrf&#x3D;b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]
 **x_csrf** | **string**| e.g. b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]

### Return type

[**\Swagger\Client\Model\PrivateForecastTimeResponse**](../Model/PrivateForecastTimeResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PrivateTrendSymbolGet**
> \Swagger\Client\Model\PublicTrendResponse v1PrivateTrendSymbolGet($symbol, $cookie, $x_csrf)

Trend

The trend response contains a collection of forecasts for different intervals with the following attributes.  + `time_start` start time of the period the forecast is applicable for  + `time_end` end time of the period the forecast is applicable for  + `interval` interval in hours that the forecast is applicable for  + `weighted_price` forecasted weighted price during the period  + `change_pct` percent change in price for forecasted weighted_price relative to current price  + `change_usd` dollar change in price for forecasted weighted_price relative to current price

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: oauth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PrivateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$symbol = "btc"; // string | The cryptocurrency symbol.
$cookie = "csrf=b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. csrf=b1820141-1bad-4a9c-93c0-52022817ce89
$x_csrf = "b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. b1820141-1bad-4a9c-93c0-52022817ce89

try {
    $result = $apiInstance->v1PrivateTrendSymbolGet($symbol, $cookie, $x_csrf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateApi->v1PrivateTrendSymbolGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**| The cryptocurrency symbol. |
 **cookie** | **string**| e.g. csrf&#x3D;b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]
 **x_csrf** | **string**| e.g. b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]

### Return type

[**\Swagger\Client\Model\PublicTrendResponse**](../Model/PublicTrendResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1PrivateTrendTabularGet**
> \Swagger\Client\Model\PrivateTrendTabularResponse v1PrivateTrendTabularGet($cookie, $x_csrf)

Trend Tabular

The trend tabular response contains a collection of forecasts for all supported cryptocurrencies at different intervals with the following attributes.  + `time_start` start time of the period the forecast is applicable for  + `time_end` end time of the period the forecast is applicable for  + `interval` interval in hours that the forecast is applicable for  + `weighted_price` forecasted weighted price during the period  + `change_pct` percent change in price for forecasted weighted_price relative to current price  + `change_usd` dollar change in price for forecasted weighted_price relative to current price

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: oauth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PrivateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cookie = "csrf=b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. csrf=b1820141-1bad-4a9c-93c0-52022817ce89
$x_csrf = "b1820141-1bad-4a9c-93c0-52022817ce89"; // string | e.g. b1820141-1bad-4a9c-93c0-52022817ce89

try {
    $result = $apiInstance->v1PrivateTrendTabularGet($cookie, $x_csrf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateApi->v1PrivateTrendTabularGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cookie** | **string**| e.g. csrf&#x3D;b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]
 **x_csrf** | **string**| e.g. b1820141-1bad-4a9c-93c0-52022817ce89 | [optional]

### Return type

[**\Swagger\Client\Model\PrivateTrendTabularResponse**](../Model/PrivateTrendTabularResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

