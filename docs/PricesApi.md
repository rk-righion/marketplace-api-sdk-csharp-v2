# IO.Swagger.Api.PricesApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetPriceProductBySku**](PricesApi.md#getpriceproductbysku) | **GET** /products/{sku}/prices | Get price of the product
[**SavePriceProductBySku**](PricesApi.md#savepriceproductbysku) | **POST** /products/{sku}/prices | Save a newly created price of the product
[**UpdatePriceProductBySku**](PricesApi.md#updatepriceproductbysku) | **PUT** /products/{sku}/prices | Update price of the product


<a name="getpriceproductbysku"></a>
# **GetPriceProductBySku**
> InlineResponse2002 GetPriceProductBySku (string clientId, string accessToken, string sku)

Get price of the product

Returns the current list and sale prices of the searched product.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetPriceProductBySkuExample
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

            var apiInstance = new PricesApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku

            try
            {
                // Get price of the product
                InlineResponse2002 result = apiInstance.GetPriceProductBySku(clientId, accessToken, sku);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PricesApi.GetPriceProductBySku: " + e.Message );
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

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="savepriceproductbysku"></a>
# **SavePriceProductBySku**
> void SavePriceProductBySku (string clientId, string accessToken, string sku, Body4 body)

Save a newly created price of the product

Saves a new list and/or sale price of a product with no previous price set.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class SavePriceProductBySkuExample
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

            var apiInstance = new PricesApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body4(); // Body4 | Json to send a price value.

            try
            {
                // Save a newly created price of the product
                apiInstance.SavePriceProductBySku(clientId, accessToken, sku, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PricesApi.SavePriceProductBySku: " + e.Message );
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
 **body** | [**Body4**](Body4.md)| Json to send a price value. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="updatepriceproductbysku"></a>
# **UpdatePriceProductBySku**
> void UpdatePriceProductBySku (string clientId, string accessToken, string sku, Body3 body)

Update price of the product

Updates the list and/or sale price of the product.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class UpdatePriceProductBySkuExample
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

            var apiInstance = new PricesApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body3(); // Body3 | Json to send a price value.

            try
            {
                // Update price of the product
                apiInstance.UpdatePriceProductBySku(clientId, accessToken, sku, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PricesApi.UpdatePriceProductBySku: " + e.Message );
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
 **body** | [**Body3**](Body3.md)| Json to send a price value. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

