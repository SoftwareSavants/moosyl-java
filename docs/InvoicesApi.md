# InvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getInvoices**](InvoicesApi.md#getInvoices) | **GET** /invoices/ | List invoices or filter by id/external user |


<a id="getInvoices"></a>
# **getInvoices**
> InvoiceList getInvoices(id, externalUserId, subscriptionId, page, limit)

List invoices or filter by id/external user

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String id = "id_example"; // String | 
    String externalUserId = "externalUserId_example"; // String | 
    String subscriptionId = "subscriptionId_example"; // String | 
    GetProductsPageParameter page = new GetProductsPageParameter(); // GetProductsPageParameter | 
    GetProductsPageParameter limit = new GetProductsPageParameter(); // GetProductsPageParameter | 
    try {
      InvoiceList result = apiInstance.getInvoices(id, externalUserId, subscriptionId, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#getInvoices");
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
| **subscriptionId** | **String**|  | [optional] |
| **page** | [**GetProductsPageParameter**](.md)|  | [optional] |
| **limit** | [**GetProductsPageParameter**](.md)|  | [optional] |

### Return type

[**InvoiceList**](InvoiceList.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

