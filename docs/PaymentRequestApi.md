# PaymentRequestApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPaymentRequestById**](PaymentRequestApi.md#getPaymentRequestById) | **GET** /payment-request/{id} | Get payment request |
| [**getPaymentRequestByTransactionByTransactionId**](PaymentRequestApi.md#getPaymentRequestByTransactionByTransactionId) | **GET** /payment-request/by-transaction/{transactionId} | Get payment request by transaction ID |
| [**patchPaymentRequestByTransactionIdRefreshStatus**](PaymentRequestApi.md#patchPaymentRequestByTransactionIdRefreshStatus) | **PATCH** /payment-request/{transactionId}/refresh-status | Refresh payment request status |
| [**postPaymentRequest**](PaymentRequestApi.md#postPaymentRequest) | **POST** /payment-request | Create payment request |


<a id="getPaymentRequestById"></a>
# **getPaymentRequestById**
> PaymentRequestGet getPaymentRequestById(id)

Get payment request

Retrieve a payment request by ID

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentRequestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentRequestApi apiInstance = new PaymentRequestApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      PaymentRequestGet result = apiInstance.getPaymentRequestById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentRequestApi#getPaymentRequestById");
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

[**PaymentRequestGet**](PaymentRequestGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="getPaymentRequestByTransactionByTransactionId"></a>
# **getPaymentRequestByTransactionByTransactionId**
> PaymentRequestGet getPaymentRequestByTransactionByTransactionId(transactionId)

Get payment request by transaction ID

Retrieve a payment request by transaction ID

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentRequestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentRequestApi apiInstance = new PaymentRequestApi(defaultClient);
    String transactionId = "transactionId_example"; // String | 
    try {
      PaymentRequestGet result = apiInstance.getPaymentRequestByTransactionByTransactionId(transactionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentRequestApi#getPaymentRequestByTransactionByTransactionId");
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
| **transactionId** | **String**|  | |

### Return type

[**PaymentRequestGet**](PaymentRequestGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="patchPaymentRequestByTransactionIdRefreshStatus"></a>
# **patchPaymentRequestByTransactionIdRefreshStatus**
> PaymentRequestRefreshStatus patchPaymentRequestByTransactionIdRefreshStatus(transactionId)

Refresh payment request status

Refresh the status of a payment request by transaction ID. Requires secret API key.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentRequestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentRequestApi apiInstance = new PaymentRequestApi(defaultClient);
    String transactionId = "transactionId_example"; // String | 
    try {
      PaymentRequestRefreshStatus result = apiInstance.patchPaymentRequestByTransactionIdRefreshStatus(transactionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentRequestApi#patchPaymentRequestByTransactionIdRefreshStatus");
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
| **transactionId** | **String**|  | |

### Return type

[**PaymentRequestRefreshStatus**](PaymentRequestRefreshStatus.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

<a id="postPaymentRequest"></a>
# **postPaymentRequest**
> PaymentRequestGet postPaymentRequest(paymentRequestCreate)

Create payment request

Create a new payment request that can be used to collect payments. Requires secret API key.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.PaymentRequestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    PaymentRequestApi apiInstance = new PaymentRequestApi(defaultClient);
    PaymentRequestCreate paymentRequestCreate = new PaymentRequestCreate(); // PaymentRequestCreate | 
    try {
      PaymentRequestGet result = apiInstance.postPaymentRequest(paymentRequestCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentRequestApi#postPaymentRequest");
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
| **paymentRequestCreate** | [**PaymentRequestCreate**](PaymentRequestCreate.md)|  | |

### Return type

[**PaymentRequestGet**](PaymentRequestGet.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

