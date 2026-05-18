# ConnectApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteConnectRevoke**](ConnectApi.md#deleteConnectRevoke) | **DELETE** /connect/revoke | Revoke a platform connection |
| [**postConnectExchange**](ConnectApi.md#postConnectExchange) | **POST** /connect/exchange | Exchange authorization code for API credentials |


<a id="deleteConnectRevoke"></a>
# **deleteConnectRevoke**
> DeleteConnectRevoke200Response deleteConnectRevoke(deleteConnectRevokeRequest)

Revoke a platform connection

Revoke a previously authorized connection between a platform and a Moosyl account.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    DeleteConnectRevokeRequest deleteConnectRevokeRequest = new DeleteConnectRevokeRequest(); // DeleteConnectRevokeRequest | 
    try {
      DeleteConnectRevoke200Response result = apiInstance.deleteConnectRevoke(deleteConnectRevokeRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#deleteConnectRevoke");
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
| **deleteConnectRevokeRequest** | [**DeleteConnectRevokeRequest**](DeleteConnectRevokeRequest.md)|  | |

### Return type

[**DeleteConnectRevoke200Response**](DeleteConnectRevoke200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postConnectExchange"></a>
# **postConnectExchange**
> PostConnectExchange200Response postConnectExchange(postConnectExchangeRequest)

Exchange authorization code for API credentials

Exchange a short-lived authorization code (obtained from the /connect flow) for the user&#39;s publishable key, secret key, and webhook secret. A webhook will be created using the provided endpoints.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.ConnectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    ConnectApi apiInstance = new ConnectApi(defaultClient);
    PostConnectExchangeRequest postConnectExchangeRequest = new PostConnectExchangeRequest(); // PostConnectExchangeRequest | 
    try {
      PostConnectExchange200Response result = apiInstance.postConnectExchange(postConnectExchangeRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#postConnectExchange");
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
| **postConnectExchangeRequest** | [**PostConnectExchangeRequest**](PostConnectExchangeRequest.md)|  | |

### Return type

[**PostConnectExchange200Response**](PostConnectExchange200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

