# CustomersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getCustomers**](CustomersApi.md#getCustomers) | **GET** /customers/ | List customers or filter by id/external user |
| [**patchCustomersById**](CustomersApi.md#patchCustomersById) | **PATCH** /customers/{id} | Update customer |
| [**postCustomers**](CustomersApi.md#postCustomers) | **POST** /customers/ | Create customer |


<a id="getCustomers"></a>
# **getCustomers**
> CustomerList getCustomers(id, externalUserId, page, limit)

List customers or filter by id/external user

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | 
    String externalUserId = "externalUserId_example"; // String | 
    GetProductsPageParameter page = new GetProductsPageParameter(); // GetProductsPageParameter | 
    GetProductsPageParameter limit = new GetProductsPageParameter(); // GetProductsPageParameter | 
    try {
      CustomerList result = apiInstance.getCustomers(id, externalUserId, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#getCustomers");
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
| **externalUserId** | **String**|  | [optional] |
| **page** | [**GetProductsPageParameter**](.md)|  | [optional] |
| **limit** | [**GetProductsPageParameter**](.md)|  | [optional] |

### Return type

[**CustomerList**](CustomerList.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchCustomersById"></a>
# **patchCustomersById**
> CustomerGet patchCustomersById(id, customerUpdate)

Update customer

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | 
    CustomerUpdate customerUpdate = new CustomerUpdate(); // CustomerUpdate | 
    try {
      CustomerGet result = apiInstance.patchCustomersById(id, customerUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#patchCustomersById");
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
| **customerUpdate** | [**CustomerUpdate**](CustomerUpdate.md)|  | |

### Return type

[**CustomerGet**](CustomerGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postCustomers"></a>
# **postCustomers**
> CustomerGet postCustomers(customerCreate)

Create customer

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    CustomerCreate customerCreate = new CustomerCreate(); // CustomerCreate | 
    try {
      CustomerGet result = apiInstance.postCustomers(customerCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#postCustomers");
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
| **customerCreate** | [**CustomerCreate**](CustomerCreate.md)|  | |

### Return type

[**CustomerGet**](CustomerGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

