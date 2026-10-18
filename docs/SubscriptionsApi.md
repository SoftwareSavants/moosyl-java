# SubscriptionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getSubscriptions**](SubscriptionsApi.md#getSubscriptions) | **GET** /subscriptions/ | List subscriptions |
| [**getSubscriptionsByExternalUserByExternalUserId**](SubscriptionsApi.md#getSubscriptionsByExternalUserByExternalUserId) | **GET** /subscriptions/by-external-user/{externalUserId} | Get subscription by external user |
| [**getSubscriptionsById**](SubscriptionsApi.md#getSubscriptionsById) | **GET** /subscriptions/{id} | Get subscription |
| [**postSubscriptions**](SubscriptionsApi.md#postSubscriptions) | **POST** /subscriptions/ | Create subscription |
| [**postSubscriptionsByExternalUser**](SubscriptionsApi.md#postSubscriptionsByExternalUser) | **POST** /subscriptions/by-external-user | Create subscription by external user |
| [**postSubscriptionsByIdCancel**](SubscriptionsApi.md#postSubscriptionsByIdCancel) | **POST** /subscriptions/{id}/cancel | Cancel subscription |


<a id="getSubscriptions"></a>
# **getSubscriptions**
> SubscriptionList getSubscriptions(status, page, limit)

List subscriptions

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String status = "trialing"; // String | 
    GetProductsPageParameter page = new GetProductsPageParameter(); // GetProductsPageParameter | 
    GetProductsPageParameter limit = new GetProductsPageParameter(); // GetProductsPageParameter | 
    try {
      SubscriptionList result = apiInstance.getSubscriptions(status, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#getSubscriptions");
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
| **status** | **String**|  | [optional] [enum: trialing, active, past_due, paused, cancelled, expired, pending_cancellation] |
| **page** | [**GetProductsPageParameter**](.md)|  | [optional] |
| **limit** | [**GetProductsPageParameter**](.md)|  | [optional] |

### Return type

[**SubscriptionList**](SubscriptionList.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="getSubscriptionsByExternalUserByExternalUserId"></a>
# **getSubscriptionsByExternalUserByExternalUserId**
> SubscriptionGet getSubscriptionsByExternalUserByExternalUserId(externalUserId)

Get subscription by external user

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String externalUserId = "externalUserId_example"; // String | 
    try {
      SubscriptionGet result = apiInstance.getSubscriptionsByExternalUserByExternalUserId(externalUserId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#getSubscriptionsByExternalUserByExternalUserId");
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
| **externalUserId** | **String**|  | |

### Return type

[**SubscriptionGet**](SubscriptionGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="getSubscriptionsById"></a>
# **getSubscriptionsById**
> SubscriptionGet getSubscriptionsById(id)

Get subscription

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SubscriptionGet result = apiInstance.getSubscriptionsById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#getSubscriptionsById");
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

[**SubscriptionGet**](SubscriptionGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postSubscriptions"></a>
# **postSubscriptions**
> SubscriptionGet postSubscriptions(subscriptionCreate)

Create subscription

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    SubscriptionCreate subscriptionCreate = new SubscriptionCreate(); // SubscriptionCreate | 
    try {
      SubscriptionGet result = apiInstance.postSubscriptions(subscriptionCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#postSubscriptions");
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
| **subscriptionCreate** | [**SubscriptionCreate**](SubscriptionCreate.md)|  | |

### Return type

[**SubscriptionGet**](SubscriptionGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postSubscriptionsByExternalUser"></a>
# **postSubscriptionsByExternalUser**
> SubscriptionGet postSubscriptionsByExternalUser(subscriptionCreateByExternalUser)

Create subscription by external user

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    SubscriptionCreateByExternalUser subscriptionCreateByExternalUser = new SubscriptionCreateByExternalUser(); // SubscriptionCreateByExternalUser | 
    try {
      SubscriptionGet result = apiInstance.postSubscriptionsByExternalUser(subscriptionCreateByExternalUser);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#postSubscriptionsByExternalUser");
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
| **subscriptionCreateByExternalUser** | [**SubscriptionCreateByExternalUser**](SubscriptionCreateByExternalUser.md)|  | |

### Return type

[**SubscriptionGet**](SubscriptionGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postSubscriptionsByIdCancel"></a>
# **postSubscriptionsByIdCancel**
> SubscriptionGet postSubscriptionsByIdCancel(id)

Cancel subscription

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SubscriptionGet result = apiInstance.postSubscriptionsByIdCancel(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#postSubscriptionsByIdCancel");
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

[**SubscriptionGet**](SubscriptionGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

