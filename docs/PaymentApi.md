# PaymentApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPaymentById**](PaymentApi.md#getPaymentById) | **GET** /payment/{id} | Get payment details |
| [**getPaymentByIdStatus**](PaymentApi.md#getPaymentByIdStatus) | **GET** /payment/{id}/status | Get payment status (heartbeat) |
| [**postPayment**](PaymentApi.md#postPayment) | **POST** /payment | Create a new payment |
| [**postPaymentByIdSimulateTransfer**](PaymentApi.md#postPaymentByIdSimulateTransfer) | **POST** /payment/{id}/simulate-transfer | Simulate a Gimtel transfer (sandbox) |


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

<a id="getPaymentByIdStatus"></a>
# **getPaymentByIdStatus**
> GetPaymentByIdStatus200Response getPaymentByIdStatus(id)

Get payment status (heartbeat)

Returns the payment&#39;s status. For Gimtel payments, poll this every few seconds while the payer is on the payment screen: the payment stops being claimable about 10 minutes after the last poll.

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
      GetPaymentByIdStatus200Response result = apiInstance.getPaymentByIdStatus(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentApi#getPaymentByIdStatus");
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

[**GetPaymentByIdStatus200Response**](GetPaymentByIdStatus200Response.md)

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

Use this endpoint to create a new payment for an existing payment request.  **Testing (Sandbox Environment Only) — native methods only**  The magic phone numbers below only apply to native payment methods (e.g. Sedad, NexConnect, native Bankily). They do not apply to Gimtel methods — see below.  | Phone Number | Status     | |--------------|------------| | 22222222     | Accepted   | | 33333333     | Accepted   | | 44444444     | Accepted   | | Other        | Rejected   |  **Gimtel methods (Bankily via Gimtel, BCI Pay, Amanty)**  The payment is created as &#x60;pending&#x60; and the response includes &#x60;instructions&#x60; (receiving phone, exact amount). The payer transfers from the phone number you sent. Poll &#x60;GET /payment/{paymentId}/status&#x60; every few seconds while the payer is on the payment screen — the payment stops being claimable about 10 minutes after the last poll. Completion also fires the &#x60;payment-updated&#x60; webhook.  In sandbox, Gimtel methods are never completed by a magic phone number: call &#x60;POST /payment/{paymentId}/simulate-transfer&#x60; instead to simulate the payer&#39;s bank transfer and complete the payment.

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

<a id="postPaymentByIdSimulateTransfer"></a>
# **postPaymentByIdSimulateTransfer**
> PostPaymentByIdSimulateTransfer200Response postPaymentByIdSimulateTransfer(id)

Simulate a Gimtel transfer (sandbox)

Sandbox only. Completes a pending Gimtel payment as if the payer had transferred the exact amount.

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
      PostPaymentByIdSimulateTransfer200Response result = apiInstance.postPaymentByIdSimulateTransfer(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentApi#postPaymentByIdSimulateTransfer");
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

[**PostPaymentByIdSimulateTransfer200Response**](PostPaymentByIdSimulateTransfer200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

