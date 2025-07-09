# PresenceApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDPresenceExtensionPut**](PresenceApi.md#v1AccountAccountIDPresenceExtensionPut) | **PUT** /v1/account/{accountID}/presence/{extension} | Set/Reset Presence for Extension |
| [**v1AccountAccountIDPresenceGet**](PresenceApi.md#v1AccountAccountIDPresenceGet) | **GET** /v1/account/{accountID}/presence | Get Presence Details |
| [**v1AccountAccountIDUserUserIDPresencePut**](PresenceApi.md#v1AccountAccountIDUserUserIDPresencePut) | **PUT** /v1/account/{accountID}/user/{userID}/presence | Set/Reset Presence for User |


<a id="v1AccountAccountIDPresenceExtensionPut"></a>
# **v1AccountAccountIDPresenceExtensionPut**
> ServiceAPIResponse v1AccountAccountIDPresenceExtensionPut(accountID, extension, reqBody)

Set/Reset Presence for Extension

Set or reset the presence status of an extension.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PresenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PresenceApi apiInstance = new PresenceApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String extension = "extension_example"; // String | Extension
    ServiceVOIPPresenceSetResetEditData reqBody = new ServiceVOIPPresenceSetResetEditData(); // ServiceVOIPPresenceSetResetEditData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDPresenceExtensionPut(accountID, extension, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PresenceApi#v1AccountAccountIDPresenceExtensionPut");
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
| **extension** | **String**| Extension | |
| **reqBody** | [**ServiceVOIPPresenceSetResetEditData**](ServiceVOIPPresenceSetResetEditData.md)| payload fields | |

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

<a id="v1AccountAccountIDPresenceGet"></a>
# **v1AccountAccountIDPresenceGet**
> ServiceDocsPresenceGet v1AccountAccountIDPresenceGet(accountID)

Get Presence Details

Retrieve details of presence subscriptions in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PresenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PresenceApi apiInstance = new PresenceApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsPresenceGet result = apiInstance.v1AccountAccountIDPresenceGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PresenceApi#v1AccountAccountIDPresenceGet");
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

[**ServiceDocsPresenceGet**](ServiceDocsPresenceGet.md)

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

<a id="v1AccountAccountIDUserUserIDPresencePut"></a>
# **v1AccountAccountIDUserUserIDPresencePut**
> ServiceAPIResponse v1AccountAccountIDUserUserIDPresencePut(accountID, userID, reqBody)

Set/Reset Presence for User

Set or reset the presence status of a user within an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PresenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PresenceApi apiInstance = new PresenceApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String userID = "userID_example"; // String | User ID, 32 alpha numeric
    ServiceVOIPPresenceSetResetEditData reqBody = new ServiceVOIPPresenceSetResetEditData(); // ServiceVOIPPresenceSetResetEditData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDUserUserIDPresencePut(accountID, userID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PresenceApi#v1AccountAccountIDUserUserIDPresencePut");
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
| **reqBody** | [**ServiceVOIPPresenceSetResetEditData**](ServiceVOIPPresenceSetResetEditData.md)| payload fields | |

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

