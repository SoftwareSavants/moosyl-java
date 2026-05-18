# MasriviApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**postMasriviInitiate**](MasriviApi.md#postMasriviInitiate) | **POST** /masrivi/initiate | Initiate Masrivi payment |


<a id="postMasriviInitiate"></a>
# **postMasriviInitiate**
> PostMasriviInitiate200Response postMasriviInitiate(postMasriviInitiateRequest)

Initiate Masrivi payment

Creates a pending payment and returns form data to redirect customer to Masrivi payment page.

### Example
```java
// Import classes:
import com.moosyl.ApiClient;
import com.moosyl.ApiException;
import com.moosyl.Configuration;
import com.moosyl.auth.*;
import com.moosyl.models.*;
import com.moosyl.api.MasriviApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure API key authorization: ApiKey
    ApiKeyAuth ApiKey = (ApiKeyAuth) defaultClient.getAuthentication("ApiKey");
    ApiKey.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKey.setApiKeyPrefix("Token");

    MasriviApi apiInstance = new MasriviApi(defaultClient);
    PostMasriviInitiateRequest postMasriviInitiateRequest = new PostMasriviInitiateRequest(); // PostMasriviInitiateRequest | 
    try {
      PostMasriviInitiate200Response result = apiInstance.postMasriviInitiate(postMasriviInitiateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MasriviApi#postMasriviInitiate");
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
| **postMasriviInitiateRequest** | [**PostMasriviInitiateRequest**](PostMasriviInitiateRequest.md)|  | |

### Return type

[**PostMasriviInitiate200Response**](PostMasriviInitiate200Response.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response for status 200 |  -  |

