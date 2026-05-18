# PaymentApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPaymentById**](PaymentApi.md#getPaymentById) | **GET** /payment/{id} | Get payment details |
| [**postPayment**](PaymentApi.md#postPayment) | **POST** /payment | Create a new payment |


<a id="getPaymentById"></a>
# **getPaymentById**
> PaymentGet getPaymentById(id)

Get payment details

Retrieve detailed information about a payment by transaction ID. Requires secret API key.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentApi apiInstance = new PaymentApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      PaymentGet result = apiInstance.getPaymentById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentApi#getPaymentById");
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

[**PaymentGet**](PaymentGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postPayment"></a>
# **postPayment**
> PostPayment200Response postPayment(paymentCreate)

Create a new payment

Use this endpoint to create a new payment for an existing payment request.  **Testing (Sandbox Environment Only)**  | Phone Number | Status     | |--------------|------------| | 22222222     | Accepted   | | 33333333     | Accepted   | | 44444444     | Accepted   | | Other        | Rejected   |

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentApi apiInstance = new PaymentApi(defaultClient);
    PaymentCreate paymentCreate = new PaymentCreate(); // PaymentCreate | 
    try {
      PostPayment200Response result = apiInstance.postPayment(paymentCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentApi#postPayment");
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
| **paymentCreate** | [**PaymentCreate**](PaymentCreate.md)|  | |

### Return type

[**PostPayment200Response**](PostPayment200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

