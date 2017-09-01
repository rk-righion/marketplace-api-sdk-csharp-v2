# IO.Swagger.Api.StocksApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetStockProductBySku**](StocksApi.md#getstockproductbysku) | **GET** /products/{sku}/stocks | Get stock of the product
[**SaveStockProductBySku**](StocksApi.md#savestockproductbysku) | **POST** /products/{sku}/stocks | Save a newly created stock quantity of the product
[**UpdateStockProductBySku**](StocksApi.md#updatestockproductbysku) | **PUT** /products/{sku}/stocks | Update stock of the product


<a name="getstockproductbysku"></a>
# **GetStockProductBySku**
> InlineResponse2003 GetStockProductBySku (string clientId, string accessToken, string sku)

Get stock of the product

Returns the current stock quantity of the product.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetStockProductBySkuExample
    {
        public void main()
        {
            
            // Configure API key authorization: access_token
            Configuration.Default.ApiKey.Add("access_token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("access_token", "Bearer");
            // Configure API key authorization: client_id
            Configuration.Default.ApiKey.Add("client_id", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("client_id", "Bearer");

            var apiInstance = new StocksApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku

            try
            {
                // Get stock of the product
                InlineResponse2003 result = apiInstance.GetStockProductBySku(clientId, accessToken, sku);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StocksApi.GetStockProductBySku: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientId** | **string**| The APP Token used to authenticate. | 
 **accessToken** | **string**| The Access Token used to authenticate. | 
 **sku** | **string**| Product&#39;s Sku | 

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="savestockproductbysku"></a>
# **SaveStockProductBySku**
> void SaveStockProductBySku (string clientId, string accessToken, string sku, Body6 body)

Save a newly created stock quantity of the product

Saves a new stock quantity of a product with no previous stock set.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class SaveStockProductBySkuExample
    {
        public void main()
        {
            
            // Configure API key authorization: access_token
            Configuration.Default.ApiKey.Add("access_token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("access_token", "Bearer");
            // Configure API key authorization: client_id
            Configuration.Default.ApiKey.Add("client_id", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("client_id", "Bearer");

            var apiInstance = new StocksApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body6(); // Body6 | Json to send a stock quantity.

            try
            {
                // Save a newly created stock quantity of the product
                apiInstance.SaveStockProductBySku(clientId, accessToken, sku, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StocksApi.SaveStockProductBySku: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientId** | **string**| The APP Token used to authenticate. | 
 **accessToken** | **string**| The Access Token used to authenticate. | 
 **sku** | **string**| Product&#39;s Sku | 
 **body** | [**Body6**](Body6.md)| Json to send a stock quantity. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="updatestockproductbysku"></a>
# **UpdateStockProductBySku**
> void UpdateStockProductBySku (string clientId, string accessToken, string sku, Body5 body)

Update stock of the product

Updates the stock quantity of the product.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class UpdateStockProductBySkuExample
    {
        public void main()
        {
            
            // Configure API key authorization: access_token
            Configuration.Default.ApiKey.Add("access_token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("access_token", "Bearer");
            // Configure API key authorization: client_id
            Configuration.Default.ApiKey.Add("client_id", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("client_id", "Bearer");

            var apiInstance = new StocksApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body5(); // Body5 | Json to send a stock quantity.

            try
            {
                // Update stock of the product
                apiInstance.UpdateStockProductBySku(clientId, accessToken, sku, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StocksApi.UpdateStockProductBySku: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientId** | **string**| The APP Token used to authenticate. | 
 **accessToken** | **string**| The Access Token used to authenticate. | 
 **sku** | **string**| Product&#39;s Sku | 
 **body** | [**Body5**](Body5.md)| Json to send a stock quantity. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

