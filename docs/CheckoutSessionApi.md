# CheckoutSessionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getCheckoutSessionPublicById**](CheckoutSessionApi.md#getCheckoutSessionPublicById) | **GET** /checkout-session/public/{id} | Get public checkout session |
| [**postCheckoutSession**](CheckoutSessionApi.md#postCheckoutSession) | **POST** /checkout-session | Create checkout session |
| [**postCheckoutSessionPublicByIdPay**](CheckoutSessionApi.md#postCheckoutSessionPublicByIdPay) | **POST** /checkout-session/public/{id}/pay | Pay public checkout session |
| [**postCheckoutSessionPublicByIdSwitchMethod**](CheckoutSessionApi.md#postCheckoutSessionPublicByIdSwitchMethod) | **POST** /checkout-session/public/{id}/switch-method | Switch public checkout method |


<a id="getCheckoutSessionPublicById"></a>
# **getCheckoutSessionPublicById**
> CheckoutSessionGet getCheckoutSessionPublicById(id)

Get public checkout session

Get checkout session details without an API key.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.models.*;
import com.moosyl.api.CheckoutSessionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CheckoutSessionApi apiInstance = new CheckoutSessionApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      CheckoutSessionGet result = apiInstance.getCheckoutSessionPublicById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutSessionApi#getCheckoutSessionPublicById");
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

[**CheckoutSessionGet**](CheckoutSessionGet.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postCheckoutSession"></a>
# **postCheckoutSession**
> CheckoutSessionCreate postCheckoutSession(checkoutSessionCreateBody)

Create checkout session

Create a hosted checkout session from paymentRequestId, or from transactionId (optionally creating the payment request when amount is provided).

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.CheckoutSessionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    CheckoutSessionApi apiInstance = new CheckoutSessionApi(defaultClient);
    CheckoutSessionCreateBody checkoutSessionCreateBody = new CheckoutSessionCreateBody(); // CheckoutSessionCreateBody | 
    try {
      CheckoutSessionCreate result = apiInstance.postCheckoutSession(checkoutSessionCreateBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutSessionApi#postCheckoutSession");
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
| **checkoutSessionCreateBody** | [**CheckoutSessionCreateBody**](CheckoutSessionCreateBody.md)|  | |

### Return type

[**CheckoutSessionCreate**](CheckoutSessionCreate.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postCheckoutSessionPublicByIdPay"></a>
# **postCheckoutSessionPublicByIdPay**
> PostCheckoutSessionPublicByIdPay200Response postCheckoutSessionPublicByIdPay(id, checkoutSessionPayBody)

Pay public checkout session

Create payment for a checkout session without requiring API key in the client.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.models.*;
import com.moosyl.api.CheckoutSessionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CheckoutSessionApi apiInstance = new CheckoutSessionApi(defaultClient);
    String id = "id_example"; // String | 
    CheckoutSessionPayBody checkoutSessionPayBody = new CheckoutSessionPayBody(); // CheckoutSessionPayBody | 
    try {
      PostCheckoutSessionPublicByIdPay200Response result = apiInstance.postCheckoutSessionPublicByIdPay(id, checkoutSessionPayBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutSessionApi#postCheckoutSessionPublicByIdPay");
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
| **checkoutSessionPayBody** | [**CheckoutSessionPayBody**](CheckoutSessionPayBody.md)|  | |

### Return type

[**PostCheckoutSessionPublicByIdPay200Response**](PostCheckoutSessionPublicByIdPay200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postCheckoutSessionPublicByIdSwitchMethod"></a>
# **postCheckoutSessionPublicByIdSwitchMethod**
> CheckoutSessionSwitchMethod postCheckoutSessionPublicByIdSwitchMethod(id, checkoutSessionSelectMethodBody)

Switch public checkout method

Switch checkout method and cancel the latest pending payment when present.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.models.*;
import com.moosyl.api.CheckoutSessionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CheckoutSessionApi apiInstance = new CheckoutSessionApi(defaultClient);
    String id = "id_example"; // String | 
    CheckoutSessionSelectMethodBody checkoutSessionSelectMethodBody = new CheckoutSessionSelectMethodBody(); // CheckoutSessionSelectMethodBody | 
    try {
      CheckoutSessionSwitchMethod result = apiInstance.postCheckoutSessionPublicByIdSwitchMethod(id, checkoutSessionSelectMethodBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutSessionApi#postCheckoutSessionPublicByIdSwitchMethod");
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
| **checkoutSessionSelectMethodBody** | [**CheckoutSessionSelectMethodBody**](CheckoutSessionSelectMethodBody.md)|  | |

### Return type

[**CheckoutSessionSwitchMethod**](CheckoutSessionSwitchMethod.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

