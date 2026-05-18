# PricesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPricesById**](PricesApi.md#getPricesById) | **GET** /prices/{id} | Get price |
| [**patchPricesById**](PricesApi.md#patchPricesById) | **PATCH** /prices/{id} | Update price |
| [**patchPricesByIdArchive**](PricesApi.md#patchPricesByIdArchive) | **PATCH** /prices/{id}/archive | Archive price |
| [**postPrices**](PricesApi.md#postPrices) | **POST** /prices/ | Create price |


<a id="getPricesById"></a>
# **getPricesById**
> PriceGet getPricesById(id)

Get price

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PricesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PricesApi apiInstance = new PricesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      PriceGet result = apiInstance.getPricesById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PricesApi#getPricesById");
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

[**PriceGet**](PriceGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchPricesById"></a>
# **patchPricesById**
> PriceGet patchPricesById(id, priceUpdate)

Update price

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PricesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PricesApi apiInstance = new PricesApi(defaultClient);
    String id = "id_example"; // String | 
    PriceUpdate priceUpdate = new PriceUpdate(); // PriceUpdate | 
    try {
      PriceGet result = apiInstance.patchPricesById(id, priceUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PricesApi#patchPricesById");
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
| **priceUpdate** | [**PriceUpdate**](PriceUpdate.md)|  | |

### Return type

[**PriceGet**](PriceGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchPricesByIdArchive"></a>
# **patchPricesByIdArchive**
> Success patchPricesByIdArchive(id)

Archive price

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PricesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PricesApi apiInstance = new PricesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      Success result = apiInstance.patchPricesByIdArchive(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PricesApi#patchPricesByIdArchive");
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

<a id="postPrices"></a>
# **postPrices**
> PriceGet postPrices(priceCreate)

Create price

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PricesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PricesApi apiInstance = new PricesApi(defaultClient);
    PriceCreate priceCreate = new PriceCreate(); // PriceCreate | 
    try {
      PriceGet result = apiInstance.postPrices(priceCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PricesApi#postPrices");
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
| **priceCreate** | [**PriceCreate**](PriceCreate.md)|  | |

### Return type

[**PriceGet**](PriceGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

