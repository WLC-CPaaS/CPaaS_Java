# CallflowApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDCallflowCallflowIDDelete**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDDelete) | **DELETE** /v1/account/{accountID}/callflow/{callflowID} | Delete Call Group |
| [**v1AccountAccountIDCallflowCallflowIDGet**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDGet) | **GET** /v1/account/{accountID}/callflow/{callflowID} | Get Call Group Details |
| [**v1AccountAccountIDCallflowCallflowIDPut**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDPut) | **PUT** /v1/account/{accountID}/callflow/{callflowID} | Update Call Group |
| [**v1AccountAccountIDCallflowGet**](CallflowApi.md#v1AccountAccountIDCallflowGet) | **GET** /v1/account/{accountID}/callflow | Get Callflow List |
| [**v1AccountAccountIDCallflowPost**](CallflowApi.md#v1AccountAccountIDCallflowPost) | **POST** /v1/account/{accountID}/callflow | Create Call Group |


<a id="v1AccountAccountIDCallflowCallflowIDDelete"></a>
# **v1AccountAccountIDCallflowCallflowIDDelete**
> ServiceDocsCallflowGetSingle v1AccountAccountIDCallflowCallflowIDDelete(accountID, callflowID)

Delete Call Group

Delete a callflow in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallflowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallflowApi apiInstance = new CallflowApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String callflowID = "callflowID_example"; // String | callflow ID, 32 alpha numeric
    try {
      ServiceDocsCallflowGetSingle result = apiInstance.v1AccountAccountIDCallflowCallflowIDDelete(accountID, callflowID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallflowApi#v1AccountAccountIDCallflowCallflowIDDelete");
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
| **callflowID** | **String**| callflow ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallflowGetSingle**](ServiceDocsCallflowGetSingle.md)

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

<a id="v1AccountAccountIDCallflowCallflowIDGet"></a>
# **v1AccountAccountIDCallflowCallflowIDGet**
> ServiceDocsCallflowGetSingle v1AccountAccountIDCallflowCallflowIDGet(accountID, callflowID)

Get Call Group Details

Get the details for a single callflow in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallflowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallflowApi apiInstance = new CallflowApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String callflowID = "callflowID_example"; // String | Callflow ID, 32 alpha numeric
    try {
      ServiceDocsCallflowGetSingle result = apiInstance.v1AccountAccountIDCallflowCallflowIDGet(accountID, callflowID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallflowApi#v1AccountAccountIDCallflowCallflowIDGet");
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
| **callflowID** | **String**| Callflow ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallflowGetSingle**](ServiceDocsCallflowGetSingle.md)

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

<a id="v1AccountAccountIDCallflowCallflowIDPut"></a>
# **v1AccountAccountIDCallflowCallflowIDPut**
> ServiceDocsCallflowGetSingle v1AccountAccountIDCallflowCallflowIDPut(accountID, callflowID, reqBody)

Update Call Group

Update the details for a single callflow in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallflowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallflowApi apiInstance = new CallflowApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String callflowID = "callflowID_example"; // String | Callflow ID, 32 alpha numeric
    ServiceCallflowAddEditData reqBody = new ServiceCallflowAddEditData(); // ServiceCallflowAddEditData | payload fields
    try {
      ServiceDocsCallflowGetSingle result = apiInstance.v1AccountAccountIDCallflowCallflowIDPut(accountID, callflowID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallflowApi#v1AccountAccountIDCallflowCallflowIDPut");
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
| **callflowID** | **String**| Callflow ID, 32 alpha numeric | |
| **reqBody** | [**ServiceCallflowAddEditData**](ServiceCallflowAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsCallflowGetSingle**](ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDCallflowGet"></a>
# **v1AccountAccountIDCallflowGet**
> ServiceDocsCallflowGetAll v1AccountAccountIDCallflowGet(accountID, startKey, pageSize)

Get Callflow List

Permit a user to view the callflow details in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallflowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallflowApi apiInstance = new CallflowApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsCallflowGetAll result = apiInstance.v1AccountAccountIDCallflowGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallflowApi#v1AccountAccountIDCallflowGet");
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
| **startKey** | **String**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **pageSize** | **Integer**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**ServiceDocsCallflowGetAll**](ServiceDocsCallflowGetAll.md)

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

<a id="v1AccountAccountIDCallflowPost"></a>
# **v1AccountAccountIDCallflowPost**
> ServiceDocsCallflowGetSingle v1AccountAccountIDCallflowPost(accountID, request)

Create Call Group

Create instructions for routing a call to a user or system.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallflowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallflowApi apiInstance = new CallflowApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha-numeric
    ServiceCallflowAddEditData request = new ServiceCallflowAddEditData(); // ServiceCallflowAddEditData | Call flow configuration
    try {
      ServiceDocsCallflowGetSingle result = apiInstance.v1AccountAccountIDCallflowPost(accountID, request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallflowApi#v1AccountAccountIDCallflowPost");
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
| **accountID** | **String**| Account ID, 32 alpha-numeric | |
| **request** | [**ServiceCallflowAddEditData**](ServiceCallflowAddEditData.md)| Call flow configuration | |

### Return type

[**ServiceDocsCallflowGetSingle**](ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

