# ProductsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getProducts**](ProductsApi.md#getProducts) | **GET** /products/ | List products or filter by id |
| [**getProductsById**](ProductsApi.md#getProductsById) | **GET** /products/{id} | Get product with prices |
| [**patchProductsById**](ProductsApi.md#patchProductsById) | **PATCH** /products/{id} | Update product |
| [**patchProductsByIdArchive**](ProductsApi.md#patchProductsByIdArchive) | **PATCH** /products/{id}/archive | Archive product |
| [**postProducts**](ProductsApi.md#postProducts) | **POST** /products/ | Create product |


<a id="getProducts"></a>
# **getProducts**
> ProductList getProducts(id, page, limit)

List products or filter by id

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | 
    GetProductsPageParameter page = new GetProductsPageParameter(); // GetProductsPageParameter | 
    GetProductsPageParameter limit = new GetProductsPageParameter(); // GetProductsPageParameter | 
    try {
      ProductList result = apiInstance.getProducts(id, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#getProducts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | [optional] |
| **page** | [**GetProductsPageParameter**](.md)|  | [optional] |
| **limit** | [**GetProductsPageParameter**](.md)|  | [optional] |

### Return type

[**ProductList**](ProductList.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="getProductsById"></a>
# **getProductsById**
> ProductGetWithPrices getProductsById(id)

Get product with prices

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      ProductGetWithPrices result = apiInstance.getProductsById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#getProductsById");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

[**ProductGetWithPrices**](ProductGetWithPrices.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchProductsById"></a>
# **patchProductsById**
> ProductGet patchProductsById(id, productUpdate)

Update product

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | 
    ProductUpdate productUpdate = new ProductUpdate(); // ProductUpdate | 
    try {
      ProductGet result = apiInstance.patchProductsById(id, productUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#patchProductsById");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |
| **productUpdate** | [**ProductUpdate**](ProductUpdate.md)|  | |

### Return type

[**ProductGet**](ProductGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchProductsByIdArchive"></a>
# **patchProductsByIdArchive**
> Success patchProductsByIdArchive(id)

Archive product

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      Success result = apiInstance.patchProductsByIdArchive(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#patchProductsByIdArchive");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

[**Success**](Success.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postProducts"></a>
# **postProducts**
> ProductGet postProducts(productCreate)

Create product

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    ProductCreate productCreate = new ProductCreate(); // ProductCreate | 
    try {
      ProductGet result = apiInstance.postProducts(productCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#postProducts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **productCreate** | [**ProductCreate**](ProductCreate.md)|  | |

### Return type

[**ProductGet**](ProductGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

