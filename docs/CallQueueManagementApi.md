# CallQueueManagementApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDCallqueueGet**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueGet) | **GET** /v1/account/{accountID}/callqueue | Get Call Queues |
| [**v1AccountAccountIDCallqueuePost**](CallQueueManagementApi.md#v1AccountAccountIDCallqueuePost) | **POST** /v1/account/{accountID}/callqueue | Create Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDDelete**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDDelete) | **DELETE** /v1/account/{accountID}/callqueue/{queueID} | Delete Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDGet**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDGet) | **GET** /v1/account/{accountID}/callqueue/{queueID} | Get Call Queue Details |
| [**v1AccountAccountIDCallqueueQueueIDPut**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDPut) | **PUT** /v1/account/{accountID}/callqueue/{queueID} | Update Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDStatusGet**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDStatusGet) | **GET** /v1/account/{accountID}/callqueue/{queueID}/status | Get Call Queue Status |
| [**v1AccountAccountIDQueuerolesGet**](CallQueueManagementApi.md#v1AccountAccountIDQueuerolesGet) | **GET** /v1/account/{accountID}/queueroles | Get Queue Roles of Account |
| [**v1AccountAccountIDQueuerolesQueueIDPost**](CallQueueManagementApi.md#v1AccountAccountIDQueuerolesQueueIDPost) | **POST** /v1/account/{accountID}/queueroles/{queueID} | Assign Queue Role to Call Queue |


<a id="v1AccountAccountIDCallqueueGet"></a>
# **v1AccountAccountIDCallqueueGet**
> ServiceDocsCallQueueGetAll v1AccountAccountIDCallqueueGet(accountID)

Get Call Queues

Retrieve call queue details for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsCallQueueGetAll result = apiInstance.v1AccountAccountIDCallqueueGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueueGet");
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

[**ServiceDocsCallQueueGetAll**](ServiceDocsCallQueueGetAll.md)

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

<a id="v1AccountAccountIDCallqueuePost"></a>
# **v1AccountAccountIDCallqueuePost**
> ServiceDocsCallQueueGetSingle v1AccountAccountIDCallqueuePost(accountID, reqBody)

Create Call Queue

Set up a call queue in an account for specific inbound calls.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPCallQueueAddEditData reqBody = new ServiceVOIPCallQueueAddEditData(); // ServiceVOIPCallQueueAddEditData | payload fields
    try {
      ServiceDocsCallQueueGetSingle result = apiInstance.v1AccountAccountIDCallqueuePost(accountID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueuePost");
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
| **reqBody** | [**ServiceVOIPCallQueueAddEditData**](ServiceVOIPCallQueueAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsCallQueueGetSingle**](ServiceDocsCallQueueGetSingle.md)

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

<a id="v1AccountAccountIDCallqueueQueueIDDelete"></a>
# **v1AccountAccountIDCallqueueQueueIDDelete**
> ServiceDocsCallQueueGetSingle v1AccountAccountIDCallqueueQueueIDDelete(accountID, queueID)

Delete Call Queue

Remove the call queue from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String queueID = "queueID_example"; // String | Queue ID, 32 alpha numeric
    try {
      ServiceDocsCallQueueGetSingle result = apiInstance.v1AccountAccountIDCallqueueQueueIDDelete(accountID, queueID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueueQueueIDDelete");
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
| **queueID** | **String**| Queue ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallQueueGetSingle**](ServiceDocsCallQueueGetSingle.md)

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

<a id="v1AccountAccountIDCallqueueQueueIDGet"></a>
# **v1AccountAccountIDCallqueueQueueIDGet**
> ServiceDocsCallQueueGetSingle v1AccountAccountIDCallqueueQueueIDGet(accountID, queueID)

Get Call Queue Details

Capture metadata about a specific queue, such as queue_type and agent_wrapup_time.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String queueID = "queueID_example"; // String | Queue ID, 32 alpha numeric
    try {
      ServiceDocsCallQueueGetSingle result = apiInstance.v1AccountAccountIDCallqueueQueueIDGet(accountID, queueID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueueQueueIDGet");
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
| **queueID** | **String**| Queue ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallQueueGetSingle**](ServiceDocsCallQueueGetSingle.md)

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

<a id="v1AccountAccountIDCallqueueQueueIDPut"></a>
# **v1AccountAccountIDCallqueueQueueIDPut**
> ServiceDocsCallQueueGetSingle v1AccountAccountIDCallqueueQueueIDPut(accountID, queueID, reqBody)

Update Call Queue

Update the metadata mentioned above.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String queueID = "queueID_example"; // String | Queue ID, 32 alpha numeric
    ServiceVOIPCallQueueAddEditData reqBody = new ServiceVOIPCallQueueAddEditData(); // ServiceVOIPCallQueueAddEditData | payload fields
    try {
      ServiceDocsCallQueueGetSingle result = apiInstance.v1AccountAccountIDCallqueueQueueIDPut(accountID, queueID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueueQueueIDPut");
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
| **queueID** | **String**| Queue ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPCallQueueAddEditData**](ServiceVOIPCallQueueAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsCallQueueGetSingle**](ServiceDocsCallQueueGetSingle.md)

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

<a id="v1AccountAccountIDCallqueueQueueIDStatusGet"></a>
# **v1AccountAccountIDCallqueueQueueIDStatusGet**
> ServiceDocsCallQueueGetSingleStatus v1AccountAccountIDCallqueueQueueIDStatusGet(accountID, queueID)

Get Call Queue Status

Access the status of a call queue in an account, such as the number of available agents (recipients), estimated wait time, and number of active sessions.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String queueID = "queueID_example"; // String | Queue ID, 32 alpha numeric
    try {
      ServiceDocsCallQueueGetSingleStatus result = apiInstance.v1AccountAccountIDCallqueueQueueIDStatusGet(accountID, queueID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDCallqueueQueueIDStatusGet");
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
| **queueID** | **String**| Queue ID, 32 alpha numeric | |

### Return type

[**ServiceDocsCallQueueGetSingleStatus**](ServiceDocsCallQueueGetSingleStatus.md)

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

<a id="v1AccountAccountIDQueuerolesGet"></a>
# **v1AccountAccountIDQueuerolesGet**
> ServiceDocsCallQueueGetRoles v1AccountAccountIDQueuerolesGet(accountID)

Get Queue Roles of Account

Obtain data about each queue role in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsCallQueueGetRoles result = apiInstance.v1AccountAccountIDQueuerolesGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDQueuerolesGet");
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

[**ServiceDocsCallQueueGetRoles**](ServiceDocsCallQueueGetRoles.md)

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

<a id="v1AccountAccountIDQueuerolesQueueIDPost"></a>
# **v1AccountAccountIDQueuerolesQueueIDPost**
> ServiceAPIResponse v1AccountAccountIDQueuerolesQueueIDPost(accountID, queueID, reqBody)

Assign Queue Role to Call Queue

Assign roles to members in a call queue.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueManagementApi apiInstance = new CallQueueManagementApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String queueID = "queueID_example"; // String | Queue ID, 32 alpha numeric
    ServiceVOIPCallQueueRoleAssignData reqBody = new ServiceVOIPCallQueueRoleAssignData(); // ServiceVOIPCallQueueRoleAssignData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDQueuerolesQueueIDPost(accountID, queueID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueManagementApi#v1AccountAccountIDQueuerolesQueueIDPost");
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
| **queueID** | **String**| Queue ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPCallQueueRoleAssignData**](ServiceVOIPCallQueueRoleAssignData.md)| payload fields | |

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

