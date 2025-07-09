# GroupApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDGroupGet**](GroupApi.md#v1AccountAccountIDGroupGet) | **GET** /v1/account/{accountID}/group | Get Group List |
| [**v1AccountAccountIDGroupGroupIDDelete**](GroupApi.md#v1AccountAccountIDGroupGroupIDDelete) | **DELETE** /v1/account/{accountID}/group/{groupID} | Delete Group |
| [**v1AccountAccountIDGroupGroupIDGet**](GroupApi.md#v1AccountAccountIDGroupGroupIDGet) | **GET** /v1/account/{accountID}/group/{groupID} | Get Group Details |
| [**v1AccountAccountIDGroupGroupIDPut**](GroupApi.md#v1AccountAccountIDGroupGroupIDPut) | **PUT** /v1/account/{accountID}/group/{groupID} | Update Group |
| [**v1AccountAccountIDGroupPost**](GroupApi.md#v1AccountAccountIDGroupPost) | **POST** /v1/account/{accountID}/group | Create Group |


<a id="v1AccountAccountIDGroupGet"></a>
# **v1AccountAccountIDGroupGet**
> ServiceDocGroupGetAll v1AccountAccountIDGroupGet(accountID, startKey, pageSize)

Get Group List

Get a list of groups associated with an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GroupApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    GroupApi apiInstance = new GroupApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocGroupGetAll result = apiInstance.v1AccountAccountIDGroupGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupApi#v1AccountAccountIDGroupGet");
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

[**ServiceDocGroupGetAll**](ServiceDocGroupGetAll.md)

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

<a id="v1AccountAccountIDGroupGroupIDDelete"></a>
# **v1AccountAccountIDGroupGroupIDDelete**
> ServiceDocGroupGetSingle v1AccountAccountIDGroupGroupIDDelete(accountID, groupID)

Delete Group

Delete a call group in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GroupApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    GroupApi apiInstance = new GroupApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String groupID = "groupID_example"; // String | group ID, 32 alpha numeric
    try {
      ServiceDocGroupGetSingle result = apiInstance.v1AccountAccountIDGroupGroupIDDelete(accountID, groupID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupApi#v1AccountAccountIDGroupGroupIDDelete");
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
| **groupID** | **String**| group ID, 32 alpha numeric | |

### Return type

[**ServiceDocGroupGetSingle**](ServiceDocGroupGetSingle.md)

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

<a id="v1AccountAccountIDGroupGroupIDGet"></a>
# **v1AccountAccountIDGroupGroupIDGet**
> ServiceDocGroupGetSingle v1AccountAccountIDGroupGroupIDGet(accountID, groupID)

Get Group Details

Access details about a single group within an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GroupApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    GroupApi apiInstance = new GroupApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String groupID = "groupID_example"; // String | Group ID, 32 alpha numeric
    try {
      ServiceDocGroupGetSingle result = apiInstance.v1AccountAccountIDGroupGroupIDGet(accountID, groupID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupApi#v1AccountAccountIDGroupGroupIDGet");
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
| **groupID** | **String**| Group ID, 32 alpha numeric | |

### Return type

[**ServiceDocGroupGetSingle**](ServiceDocGroupGetSingle.md)

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

<a id="v1AccountAccountIDGroupGroupIDPut"></a>
# **v1AccountAccountIDGroupGroupIDPut**
> ServiceDocGroupGetSingle v1AccountAccountIDGroupGroupIDPut(accountID, groupID, reqBody)

Update Group

Modify the name, settings and other information for a group within an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GroupApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    GroupApi apiInstance = new GroupApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String groupID = "groupID_example"; // String | Group ID, 32 alpha numeric
    ServiceVOIPGroupAddEdit2 reqBody = new ServiceVOIPGroupAddEdit2(); // ServiceVOIPGroupAddEdit2 | payload fields
    try {
      ServiceDocGroupGetSingle result = apiInstance.v1AccountAccountIDGroupGroupIDPut(accountID, groupID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupApi#v1AccountAccountIDGroupGroupIDPut");
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
| **groupID** | **String**| Group ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPGroupAddEdit2**](ServiceVOIPGroupAddEdit2.md)| payload fields | |

### Return type

[**ServiceDocGroupGetSingle**](ServiceDocGroupGetSingle.md)

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

<a id="v1AccountAccountIDGroupPost"></a>
# **v1AccountAccountIDGroupPost**
> ServiceDocGroupGetSingle v1AccountAccountIDGroupPost(accountID, group)

Create Group

Provide an additional resource by adding a group list to an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GroupApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    GroupApi apiInstance = new GroupApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID
    ServiceVOIPGroupAddEdit2 group = new ServiceVOIPGroupAddEdit2(); // ServiceVOIPGroupAddEdit2 | group fields
    try {
      ServiceDocGroupGetSingle result = apiInstance.v1AccountAccountIDGroupPost(accountID, group);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupApi#v1AccountAccountIDGroupPost");
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
| **accountID** | **String**| Account ID | |
| **group** | [**ServiceVOIPGroupAddEdit2**](ServiceVOIPGroupAddEdit2.md)| group fields | |

### Return type

[**ServiceDocGroupGetSingle**](ServiceDocGroupGetSingle.md)

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

