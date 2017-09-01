# IO.Swagger.Api.ProductsApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetProductBySku**](ProductsApi.md#getproductbysku) | **GET** /products/{sku} | Get product by sku
[**GetProducts**](ProductsApi.md#getproducts) | **GET** /products | Get list of products
[**GetStatusProductBySku**](ProductsApi.md#getstatusproductbysku) | **GET** /products/{sku}/status | Get product status
[**SaveProduct**](ProductsApi.md#saveproduct) | **POST** /products | Create a new product.
[**UpdateProduct**](ProductsApi.md#updateproduct) | **PUT** /products/{sku} | Update a product.
[**UpdateProductStatusBySku**](ProductsApi.md#updateproductstatusbysku) | **PUT** /products/{sku}/status | Update product status. Only sandbox


<a name="getproductbysku"></a>
# **GetProductBySku**
> InlineResponse200Items GetProductBySku (string clientId, string accessToken, string sku, string expands = null)

Get product by sku

Returns the product associated with the searched sku.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetProductBySkuExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var expands = expands_example;  // string | Expand response relationships, for instance if you need to access product images use 'images', to access product attributes use 'attributes' and to access images and attributes use 'images,attributes'. (optional) 

            try
            {
                // Get product by sku
                InlineResponse200Items result = apiInstance.GetProductBySku(clientId, accessToken, sku, expands);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.GetProductBySku: " + e.Message );
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
 **expands** | **string**| Expand response relationships, for instance if you need to access product images use &#39;images&#39;, to access product attributes use &#39;attributes&#39; and to access images and attributes use &#39;images,attributes&#39;. | [optional] 

### Return type

[**InlineResponse200Items**](InlineResponse200Items.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getproducts"></a>
# **GetProducts**
> InlineResponse200 GetProducts (string clientId, string accessToken, int? page = null, int? size = null, string expands = null)

Get list of products

Returns all products associated to the seller.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetProductsExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var page = 56;  // int? | Number of the page in pagination. The starting page number is zero. (optional)  (default to 0)
            var size = 56;  // int? | Define the size of the returned list of products. (optional)  (default to 20)
            var expands = expands_example;  // string | Expand response relationships, for instance if you need to access product images use 'images', to access product attributes use 'attributes' and to access images and attributes use 'images,attributes'. (optional) 

            try
            {
                // Get list of products
                InlineResponse200 result = apiInstance.GetProducts(clientId, accessToken, page, size, expands);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.GetProducts: " + e.Message );
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
 **page** | **int?**| Number of the page in pagination. The starting page number is zero. | [optional] [default to 0]
 **size** | **int?**| Define the size of the returned list of products. | [optional] [default to 20]
 **expands** | **string**| Expand response relationships, for instance if you need to access product images use &#39;images&#39;, to access product attributes use &#39;attributes&#39; and to access images and attributes use &#39;images,attributes&#39;. | [optional] 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getstatusproductbysku"></a>
# **GetStatusProductBySku**
> InlineResponse2001 GetStatusProductBySku (string clientId, string accessToken, string sku)

Get product status

Returns the current status of a product.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetStatusProductBySkuExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku

            try
            {
                // Get product status
                InlineResponse2001 result = apiInstance.GetStatusProductBySku(clientId, accessToken, sku);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.GetStatusProductBySku: " + e.Message );
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

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="saveproduct"></a>
# **SaveProduct**
> void SaveProduct (string clientId, string accessToken, Body body)

Create a new product.

Creates a new product. Cannot set flavor and color on the same product

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class SaveProductExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var body = new Body(); // Body | Product json to create a new product.

            try
            {
                // Create a new product.
                apiInstance.SaveProduct(clientId, accessToken, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.SaveProduct: " + e.Message );
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
 **body** | [**Body**](Body.md)| Product json to create a new product. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="updateproduct"></a>
# **UpdateProduct**
> void UpdateProduct (string clientId, string accessToken, string sku, Body1 body)

Update a product.

Updates a product. Cannot set flavor and color on the same product

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class UpdateProductExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body1(); // Body1 | Product json to create a new product.

            try
            {
                // Update a product.
                apiInstance.UpdateProduct(clientId, accessToken, sku, body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.UpdateProduct: " + e.Message );
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
 **body** | [**Body1**](Body1.md)| Product json to create a new product. | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="updateproductstatusbysku"></a>
# **UpdateProductStatusBySku**
> InlineResponse2001 UpdateProductStatusBySku (string clientId, string accessToken, string sku, Body2 body)

Update product status. Only sandbox

Update product status for Sandbox operations

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class UpdateProductStatusBySkuExample
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

            var apiInstance = new ProductsApi();
            var clientId = clientId_example;  // string | The APP Token used to authenticate.
            var accessToken = accessToken_example;  // string | The Access Token used to authenticate.
            var sku = sku_example;  // string | Product's Sku
            var body = new Body2(); // Body2 | Json to update status.

            try
            {
                // Update product status. Only sandbox
                InlineResponse2001 result = apiInstance.UpdateProductStatusBySku(clientId, accessToken, sku, body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ProductsApi.UpdateProductStatusBySku: " + e.Message );
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
 **body** | [**Body2**](Body2.md)| Json to update status. | 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[access_token](../README.md#access_token), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

