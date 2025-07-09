# CallRecordingApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDRecordingGet**](CallRecordingApi.md#v1AccountAccountIDRecordingGet) | **GET** /v1/account/{accountID}/recording | Get Account Call Recording |
| [**v1AccountAccountIDRecordingRecordingIDDelete**](CallRecordingApi.md#v1AccountAccountIDRecordingRecordingIDDelete) | **DELETE** /v1/account/{accountID}/recording/{recordingID} | Delete Call Recording |
| [**v1AccountAccountIDRecordingRecordingIDGet**](CallRecordingApi.md#v1AccountAccountIDRecordingRecordingIDGet) | **GET** /v1/account/{accountID}/recording/{recordingID} | Get Call Recording Details |
| [**v1AccountAccountIDUserUserIDRecordingGet**](CallRecordingApi.md#v1AccountAccountIDUserUserIDRecordingGet) | **GET** /v1/account/{accountID}/user/{userID}/recording | Get User Call Recording |


<a id="v1AccountAccountIDRecordingGet"></a>
# **v1AccountAccountIDRecordingGet**
> ServiceDocsCallRecordingGetAll v1AccountAccountIDRecordingGet(accountID)

Get Account Call Recording

Obtain a list of the call recordings within an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallRecordingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallRecordingApi apiInstance = new CallRecordingApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsCallRecordingGetAll result = apiInstance.v1AccountAccountIDRecordingGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallRecordingApi#v1AccountAccountIDRecordingGet");
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
| **accountID** | **String**| Account ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallRecordingGetAll**](ServiceDocsCallRecordingGetAll.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDRecordingRecordingIDDelete"></a>
# **v1AccountAccountIDRecordingRecordingIDDelete**
> ServiceDocsCallRecordingGetSingle v1AccountAccountIDRecordingRecordingIDDelete(accountID, recordingID)

Delete Call Recording

Delete a single call recording from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallRecordingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallRecordingApi apiInstance = new CallRecordingApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String recordingID = "recordingID_example"; // String | Recording ID, 39 (yyyymm-<32 id>)
    try {
      ServiceDocsCallRecordingGetSingle result = apiInstance.v1AccountAccountIDRecordingRecordingIDDelete(accountID, recordingID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallRecordingApi#v1AccountAccountIDRecordingRecordingIDDelete");
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
| **accountID** | **String**| Account ID, 32 alpha numeric | |
| **recordingID** | **String**| Recording ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**ServiceDocsCallRecordingGetSingle**](ServiceDocsCallRecordingGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDRecordingRecordingIDGet"></a>
# **v1AccountAccountIDRecordingRecordingIDGet**
> ServiceDocsCallRecordingGetSingle v1AccountAccountIDRecordingRecordingIDGet(accountID, recordingID)

Get Call Recording Details

Access details for each recorded call in an account (e.g., duration, names and numbers of call participants, etc.).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallRecordingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallRecordingApi apiInstance = new CallRecordingApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String recordingID = "recordingID_example"; // String | Recording ID, 39 (yyyymm-<32 id>)
    try {
      ServiceDocsCallRecordingGetSingle result = apiInstance.v1AccountAccountIDRecordingRecordingIDGet(accountID, recordingID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallRecordingApi#v1AccountAccountIDRecordingRecordingIDGet");
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
| **accountID** | **String**| Account ID, 32 alpha numeric | |
| **recordingID** | **String**| Recording ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**ServiceDocsCallRecordingGetSingle**](ServiceDocsCallRecordingGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, audio/mp3, audio/mpeg, audio/mpeg3, audio/x-wav, audio/wav

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDUserUserIDRecordingGet"></a>
# **v1AccountAccountIDUserUserIDRecordingGet**
> ServiceDocsCallRecordingGetAll v1AccountAccountIDUserUserIDRecordingGet(accountID, userID)

Get User Call Recording

Retrieve a list of call recordings for a user within an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallRecordingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallRecordingApi apiInstance = new CallRecordingApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String userID = "userID_example"; // String | User ID, 32 alpha numeric
    try {
      ServiceDocsCallRecordingGetAll result = apiInstance.v1AccountAccountIDUserUserIDRecordingGet(accountID, userID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallRecordingApi#v1AccountAccountIDUserUserIDRecordingGet");
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
| **accountID** | **String**| Account ID, 32 alpha numeric | |
| **userID** | **String**| User ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallRecordingGetAll**](ServiceDocsCallRecordingGetAll.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

