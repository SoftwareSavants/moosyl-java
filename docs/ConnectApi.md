# ConnectApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteConnectRevoke**](ConnectApi.md#deleteConnectRevoke) | **DELETE** /connect/revoke | Revoke a platform connection |
| [**postConnectExchange**](ConnectApi.md#postConnectExchange) | **POST** /connect/exchange | Exchange authorization code for API credentials |
| [**postConnectRevoke**](ConnectApi.md#postConnectRevoke) | **POST** /connect/revoke | Revoke a platform connection (POST) |


<a id="deleteConnectRevoke"></a>
# **deleteConnectRevoke**
> PostConnectRevoke200Response deleteConnectRevoke(postConnectRevokeRequest)

Revoke a platform connection

Revoke a connection between a platform and a Moosyl account. Deletes the connection&#39;s API keys and webhook, so the platform loses access immediately.

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
    PostConnectRevokeRequest postConnectRevokeRequest = new PostConnectRevokeRequest(); // PostConnectRevokeRequest | 
    try {
      PostConnectRevoke200Response result = apiInstance.deleteConnectRevoke(postConnectRevokeRequest);
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
| **postConnectRevokeRequest** | [**PostConnectRevokeRequest**](PostConnectRevokeRequest.md)|  | |

### Return type

[**PostConnectRevoke200Response**](PostConnectRevoke200Response.md)

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

Exchange a short-lived authorization code (obtained from the /connect flow) for API keys dedicated to this connection, a webhook secret, and the connection ID used to revoke it. Connecting again replaces the keys and updates the same webhook.

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

<a id="postConnectRevoke"></a>
# **postConnectRevoke**
> PostConnectRevoke200Response postConnectRevoke(postConnectRevokeRequest)

Revoke a platform connection (POST)

Revoke a connection between a platform and a Moosyl account. Deletes the connection&#39;s API keys and webhook, so the platform loses access immediately.

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
    PostConnectRevokeRequest postConnectRevokeRequest = new PostConnectRevokeRequest(); // PostConnectRevokeRequest | 
    try {
      PostConnectRevoke200Response result = apiInstance.postConnectRevoke(postConnectRevokeRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConnectApi#postConnectRevoke");
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
| **postConnectRevokeRequest** | [**PostConnectRevokeRequest**](PostConnectRevokeRequest.md)|  | |

### Return type

[**PostConnectRevoke200Response**](PostConnectRevoke200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

