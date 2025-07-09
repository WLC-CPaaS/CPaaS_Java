# ChannelApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDChannelChannelIDGet**](ChannelApi.md#v1AccountAccountIDChannelChannelIDGet) | **GET** /v1/account/{accountID}/channel/{channelID} | Get Channel Details |
| [**v1AccountAccountIDChannelChannelIDPost**](ChannelApi.md#v1AccountAccountIDChannelChannelIDPost) | **POST** /v1/account/{accountID}/channel/{channelID} | Associate Action to Channel |
| [**v1AccountAccountIDChannelChannelIDPut**](ChannelApi.md#v1AccountAccountIDChannelChannelIDPut) | **PUT** /v1/account/{accountID}/channel/{channelID} | Associate Metaflow to Channel |
| [**v1AccountAccountIDChannelGet**](ChannelApi.md#v1AccountAccountIDChannelGet) | **GET** /v1/account/{accountID}/channel | Get Account Channel List |
| [**v1AccountAccountIDDeviceDeviceIDChannelGet**](ChannelApi.md#v1AccountAccountIDDeviceDeviceIDChannelGet) | **GET** /v1/account/{accountID}/device/{deviceID}/channel | Get Device Channel List |
| [**v1AccountAccountIDUserUserIDChannelGet**](ChannelApi.md#v1AccountAccountIDUserUserIDChannelGet) | **GET** /v1/account/{accountID}/user/{userID}/channel | Get User Channel List |


<a id="v1AccountAccountIDChannelChannelIDGet"></a>
# **v1AccountAccountIDChannelChannelIDGet**
> ServiceDocsChannelGetSingle v1AccountAccountIDChannelChannelIDGet(accountID, channelID)

Get Channel Details

Access details about each channel in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String channelID = "channelID_example"; // String | Channel ID
    try {
      ServiceDocsChannelGetSingle result = apiInstance.v1AccountAccountIDChannelChannelIDGet(accountID, channelID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDChannelChannelIDGet");
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
| **channelID** | **String**| Channel ID | |

### Return type

[**ServiceDocsChannelGetSingle**](ServiceDocsChannelGetSingle.md)

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

<a id="v1AccountAccountIDChannelChannelIDPost"></a>
# **v1AccountAccountIDChannelChannelIDPost**
> ServiceAPIResponse v1AccountAccountIDChannelChannelIDPost(accountID, channelID, reqBody)

Associate Action to Channel

Link an action, such as transfer or hangup to a channel.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String channelID = "channelID_example"; // String | Channel ID
    ServiceVOIPChannelRunActionData reqBody = new ServiceVOIPChannelRunActionData(); // ServiceVOIPChannelRunActionData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDChannelChannelIDPost(accountID, channelID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDChannelChannelIDPost");
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
| **channelID** | **String**| Channel ID | |
| **reqBody** | [**ServiceVOIPChannelRunActionData**](ServiceVOIPChannelRunActionData.md)| payload fields | |

### Return type

[**ServiceAPIResponse**](ServiceAPIResponse.md)

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

<a id="v1AccountAccountIDChannelChannelIDPut"></a>
# **v1AccountAccountIDChannelChannelIDPut**
> ServiceAPIResponse v1AccountAccountIDChannelChannelIDPut(accountID, channelID, reqBody)

Associate Metaflow to Channel

Link a metaflow to an active channel.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String channelID = "channelID_example"; // String | Channel ID
    ServiceVOIPChannelRunMetaflowData reqBody = new ServiceVOIPChannelRunMetaflowData(); // ServiceVOIPChannelRunMetaflowData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDChannelChannelIDPut(accountID, channelID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDChannelChannelIDPut");
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
| **channelID** | **String**| Channel ID | |
| **reqBody** | [**ServiceVOIPChannelRunMetaflowData**](ServiceVOIPChannelRunMetaflowData.md)| payload fields | |

### Return type

[**ServiceAPIResponse**](ServiceAPIResponse.md)

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

<a id="v1AccountAccountIDChannelGet"></a>
# **v1AccountAccountIDChannelGet**
> ServiceDocsChannelGetAll v1AccountAccountIDChannelGet(accountID)

Get Account Channel List

Get a list of active channels for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsChannelGetAll result = apiInstance.v1AccountAccountIDChannelGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDChannelGet");
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

[**ServiceDocsChannelGetAll**](ServiceDocsChannelGetAll.md)

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

<a id="v1AccountAccountIDDeviceDeviceIDChannelGet"></a>
# **v1AccountAccountIDDeviceDeviceIDChannelGet**
> ServiceDocsChannelGetAll v1AccountAccountIDDeviceDeviceIDChannelGet(accountID, deviceID)

Get Device Channel List

Get the list of active channels for a device.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String deviceID = "deviceID_example"; // String | Device ID, 32 alpha numeric
    try {
      ServiceDocsChannelGetAll result = apiInstance.v1AccountAccountIDDeviceDeviceIDChannelGet(accountID, deviceID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDDeviceDeviceIDChannelGet");
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
| **deviceID** | **String**| Device ID, 32 alpha numeric | |

### Return type

[**ServiceDocsChannelGetAll**](ServiceDocsChannelGetAll.md)

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

<a id="v1AccountAccountIDUserUserIDChannelGet"></a>
# **v1AccountAccountIDUserUserIDChannelGet**
> ServiceDocsChannelGetAll v1AccountAccountIDUserUserIDChannelGet(accountID, userID)

Get User Channel List

Get the list of active channels for a user.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ChannelApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ChannelApi apiInstance = new ChannelApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String userID = "userID_example"; // String | User ID, 32 alpha numeric
    try {
      ServiceDocsChannelGetAll result = apiInstance.v1AccountAccountIDUserUserIDChannelGet(accountID, userID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelApi#v1AccountAccountIDUserUserIDChannelGet");
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

[**ServiceDocsChannelGetAll**](ServiceDocsChannelGetAll.md)

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

