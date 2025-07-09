# DataApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDCdrCdrIDGet**](DataApi.md#v1AccountAccountIDCdrCdrIDGet) | **GET** /v1/account/{accountID}/cdr/{cdrID} | Get CDR Details |
| [**v1AccountAccountIDCdrGet**](DataApi.md#v1AccountAccountIDCdrGet) | **GET** /v1/account/{accountID}/cdr | Get CDR List |
| [**v1DataCallDailySummaryGet**](DataApi.md#v1DataCallDailySummaryGet) | **GET** /v1/data/call_daily_summary | Get Call Daily Summary List |
| [**v1DataCallDetailGet**](DataApi.md#v1DataCallDetailGet) | **GET** /v1/data/call_detail | Get Call Detail List |
| [**v1DataCallMonthlySummaryGet**](DataApi.md#v1DataCallMonthlySummaryGet) | **GET** /v1/data/call_monthly_summary | Get Call Detail List |
| [**v1DataEndpointListGet**](DataApi.md#v1DataEndpointListGet) | **GET** /v1/data/endpoint_list | Get Endpoint List |
| [**v1DataEventDailySummaryGet**](DataApi.md#v1DataEventDailySummaryGet) | **GET** /v1/data/event_daily_summary | Get Event Daily Summary List |
| [**v1DataEventDetailGet**](DataApi.md#v1DataEventDetailGet) | **GET** /v1/data/event_detail | Get Event Details |
| [**v1DataEventMonthlySummaryGet**](DataApi.md#v1DataEventMonthlySummaryGet) | **GET** /v1/data/event_monthly_summary | Get Event Monthly Summary List |
| [**v1DataFeatureDailySummaryGet**](DataApi.md#v1DataFeatureDailySummaryGet) | **GET** /v1/data/feature_daily_summary | Get Feature Daily Summary List |
| [**v1DataFeatureMonthlySummaryGet**](DataApi.md#v1DataFeatureMonthlySummaryGet) | **GET** /v1/data/feature_monthly_summary | Get Feature Monthly Summary List |


<a id="v1AccountAccountIDCdrCdrIDGet"></a>
# **v1AccountAccountIDCdrCdrIDGet**
> ServiceDocsCdrGetSingle v1AccountAccountIDCdrCdrIDGet(accountID, cdrID)

Get CDR Details

Retrieve the details of a single CDR record from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String cdrID = "cdrID_example"; // String | CDR ID, string
    try {
      ServiceDocsCdrGetSingle result = apiInstance.v1AccountAccountIDCdrCdrIDGet(accountID, cdrID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1AccountAccountIDCdrCdrIDGet");
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
| **cdrID** | **String**| CDR ID, string | |

### Return type

[**ServiceDocsCdrGetSingle**](ServiceDocsCdrGetSingle.md)

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

<a id="v1AccountAccountIDCdrGet"></a>
# **v1AccountAccountIDCdrGet**
> ServiceDocsCdrGetAll v1AccountAccountIDCdrGet(accountID, pageSize, startKey, createdFrom, createdTo)

Get CDR List

Retrieve a list of CDRs in a specific account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String pageSize = "pageSize_example"; // String | Page size (Maximum number of results to display per page)
    String startKey = "startKey_example"; // String | Start key (Starting offset for displaying results)
    String createdFrom = "createdFrom_example"; // String | For displaying records which are created on or after this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds)
    String createdTo = "createdTo_example"; // String | For displaying records which are created on or before this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds)
    try {
      ServiceDocsCdrGetAll result = apiInstance.v1AccountAccountIDCdrGet(accountID, pageSize, startKey, createdFrom, createdTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1AccountAccountIDCdrGet");
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
| **pageSize** | **String**| Page size (Maximum number of results to display per page) | [optional] |
| **startKey** | **String**| Start key (Starting offset for displaying results) | [optional] |
| **createdFrom** | **String**| For displaying records which are created on or after this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds) | [optional] |
| **createdTo** | **String**| For displaying records which are created on or before this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds) | [optional] |

### Return type

[**ServiceDocsCdrGetAll**](ServiceDocsCdrGetAll.md)

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

<a id="v1DataCallDailySummaryGet"></a>
# **v1DataCallDailySummaryGet**
> ServiceDocsCallDailySummary v1DataCallDailySummaryGet(accountId, callType, endDate, pageSize, startDate, startKey)

Get Call Daily Summary List

Retrieve a daily summary of calls, including the account ID that made or received a call, the call type, the month and year, the duration, and other relevant information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    String callType = "callType_example"; // String | 
    String endDate = "endDate_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startDate = "startDate_example"; // String | 
    String startKey = "startKey_example"; // String | 
    try {
      ServiceDocsCallDailySummary result = apiInstance.v1DataCallDailySummaryGet(accountId, callType, endDate, pageSize, startDate, startKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataCallDailySummaryGet");
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
| **accountId** | **String**|  | [optional] |
| **callType** | **String**|  | [optional] |
| **endDate** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startDate** | **String**|  | [optional] |
| **startKey** | **String**|  | [optional] |

### Return type

[**ServiceDocsCallDailySummary**](ServiceDocsCallDailySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataCallDetailGet"></a>
# **v1DataCallDetailGet**
> ServiceDocsCallDetail v1DataCallDetailGet(account, callType, calleeName, calleeNumber, callerName, callerNumber, endDate, pageSize, startDate, startKey)

Get Call Detail List

Retrieve specific details about a call (e.g., caller, recipient, date, time, duration, etc.).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String account = "account_example"; // String | 
    String callType = "callType_example"; // String | 
    String calleeName = "calleeName_example"; // String | 
    String calleeNumber = "calleeNumber_example"; // String | 
    String callerName = "callerName_example"; // String | 
    String callerNumber = "callerNumber_example"; // String | 
    String endDate = "endDate_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startDate = "startDate_example"; // String | 
    String startKey = "startKey_example"; // String | 
    try {
      ServiceDocsCallDetail result = apiInstance.v1DataCallDetailGet(account, callType, calleeName, calleeNumber, callerName, callerNumber, endDate, pageSize, startDate, startKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataCallDetailGet");
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
| **account** | **String**|  | [optional] |
| **callType** | **String**|  | [optional] |
| **calleeName** | **String**|  | [optional] |
| **calleeNumber** | **String**|  | [optional] |
| **callerName** | **String**|  | [optional] |
| **callerNumber** | **String**|  | [optional] |
| **endDate** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startDate** | **String**|  | [optional] |
| **startKey** | **String**|  | [optional] |

### Return type

[**ServiceDocsCallDetail**](ServiceDocsCallDetail.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataCallMonthlySummaryGet"></a>
# **v1DataCallMonthlySummaryGet**
> ServiceDocsCallMonthlySummary v1DataCallMonthlySummaryGet(account, callType, endMonth, endYear, pageSize, startKey, startMonth, startYear)

Get Call Detail List

Retrieve a monthly summary of calls, including which accounts made or received calls, the call type, and other relevant information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String account = "account_example"; // String | 
    String callType = "callType_example"; // String | 
    Integer endMonth = 56; // Integer | 
    Integer endYear = 56; // Integer | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    Integer startMonth = 56; // Integer | 
    Integer startYear = 56; // Integer | 
    try {
      ServiceDocsCallMonthlySummary result = apiInstance.v1DataCallMonthlySummaryGet(account, callType, endMonth, endYear, pageSize, startKey, startMonth, startYear);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataCallMonthlySummaryGet");
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
| **account** | **String**|  | [optional] |
| **callType** | **String**|  | [optional] |
| **endMonth** | **Integer**|  | [optional] |
| **endYear** | **Integer**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **startMonth** | **Integer**|  | [optional] |
| **startYear** | **Integer**|  | [optional] |

### Return type

[**ServiceDocsCallMonthlySummary**](ServiceDocsCallMonthlySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataEndpointListGet"></a>
# **v1DataEndpointListGet**
> ServiceDocsEndpointList v1DataEndpointListGet(endpointName, featureName, pageSize, startKey, transactionType, version)

Get Endpoint List

Access the endpoint list for each CPaaS API.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String endpointName = "endpointName_example"; // String | 
    String featureName = "featureName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    String transactionType = "transactionType_example"; // String | 
    String version = "version_example"; // String | 
    try {
      ServiceDocsEndpointList result = apiInstance.v1DataEndpointListGet(endpointName, featureName, pageSize, startKey, transactionType, version);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataEndpointListGet");
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
| **endpointName** | **String**|  | [optional] |
| **featureName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **transactionType** | **String**|  | [optional] |
| **version** | **String**|  | [optional] |

### Return type

[**ServiceDocsEndpointList**](ServiceDocsEndpointList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataEventDailySummaryGet"></a>
# **v1DataEventDailySummaryGet**
> ServiceDocsEventDailySummary v1DataEventDailySummaryGet(accountId, component, endDate, pageSize, startDate, startKey)

Get Event Daily Summary List

Obtain a daily summary of events in a CPaaS account (e.g., setting/resetting the presence status for a user or extension).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    String component = "component_example"; // String | 
    String endDate = "endDate_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startDate = "startDate_example"; // String | 
    String startKey = "startKey_example"; // String | 
    try {
      ServiceDocsEventDailySummary result = apiInstance.v1DataEventDailySummaryGet(accountId, component, endDate, pageSize, startDate, startKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataEventDailySummaryGet");
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
| **accountId** | **String**|  | [optional] |
| **component** | **String**|  | [optional] |
| **endDate** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startDate** | **String**|  | [optional] |
| **startKey** | **String**|  | [optional] |

### Return type

[**ServiceDocsEventDailySummary**](ServiceDocsEventDailySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataEventDetailGet"></a>
# **v1DataEventDetailGet**
> ServiceDocsEventDetail v1DataEventDetailGet(accountId, component, endDateTime, eventName, execStatus, pageSize, startDateTime, startKey, username)

Get Event Details

Obtain specific details about an event (e.g., an E911 notification, a deleted account, or a created user).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    String component = "component_example"; // String | 
    String endDateTime = "endDateTime_example"; // String | 
    String eventName = "eventName_example"; // String | 
    String execStatus = "execStatus_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startDateTime = "startDateTime_example"; // String | 
    String startKey = "startKey_example"; // String | 
    String username = "username_example"; // String | 
    try {
      ServiceDocsEventDetail result = apiInstance.v1DataEventDetailGet(accountId, component, endDateTime, eventName, execStatus, pageSize, startDateTime, startKey, username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataEventDetailGet");
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
| **accountId** | **String**|  | [optional] |
| **component** | **String**|  | [optional] |
| **endDateTime** | **String**|  | [optional] |
| **eventName** | **String**|  | [optional] |
| **execStatus** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startDateTime** | **String**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **username** | **String**|  | [optional] |

### Return type

[**ServiceDocsEventDetail**](ServiceDocsEventDetail.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataEventMonthlySummaryGet"></a>
# **v1DataEventMonthlySummaryGet**
> ServiceDocsEventMonthlySummary v1DataEventMonthlySummaryGet(accountId, component, endMonth, endYear, pageSize, startKey, startMonth, startYear)

Get Event Monthly Summary List

Obtain a monthly summary of events in a CPaaS account (e.g., adding media files or assigning phone numbers).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String accountId = "accountId_example"; // String | 
    String component = "component_example"; // String | 
    Integer endMonth = 56; // Integer | 
    Integer endYear = 56; // Integer | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    Integer startMonth = 56; // Integer | 
    Integer startYear = 56; // Integer | 
    try {
      ServiceDocsEventMonthlySummary result = apiInstance.v1DataEventMonthlySummaryGet(accountId, component, endMonth, endYear, pageSize, startKey, startMonth, startYear);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataEventMonthlySummaryGet");
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
| **accountId** | **String**|  | [optional] |
| **component** | **String**|  | [optional] |
| **endMonth** | **Integer**|  | [optional] |
| **endYear** | **Integer**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **startMonth** | **Integer**|  | [optional] |
| **startYear** | **Integer**|  | [optional] |

### Return type

[**ServiceDocsEventMonthlySummary**](ServiceDocsEventMonthlySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataFeatureDailySummaryGet"></a>
# **v1DataFeatureDailySummaryGet**
> ServiceDocsFeatureDailySummary v1DataFeatureDailySummaryGet(endDate, featureName, pageSize, startDate, startKey)

Get Feature Daily Summary List

Retrieve a daily summary about a feature, including usage, which accounts execute the steps, and other relevant information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    String endDate = "endDate_example"; // String | 
    String featureName = "featureName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startDate = "startDate_example"; // String | 
    String startKey = "startKey_example"; // String | 
    try {
      ServiceDocsFeatureDailySummary result = apiInstance.v1DataFeatureDailySummaryGet(endDate, featureName, pageSize, startDate, startKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataFeatureDailySummaryGet");
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
| **endDate** | **String**|  | [optional] |
| **featureName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startDate** | **String**|  | [optional] |
| **startKey** | **String**|  | [optional] |

### Return type

[**ServiceDocsFeatureDailySummary**](ServiceDocsFeatureDailySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

<a id="v1DataFeatureMonthlySummaryGet"></a>
# **v1DataFeatureMonthlySummaryGet**
> ServiceDocsFeatureMonthlySummary v1DataFeatureMonthlySummaryGet(endMonth, endYear, featureName, pageSize, startKey, startMonth, startYear)

Get Feature Monthly Summary List

Retrieve a monthly summary about a feature’s usage, new users, updates, and other relevant information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    DataApi apiInstance = new DataApi(defaultClient);
    Integer endMonth = 56; // Integer | 
    Integer endYear = 56; // Integer | 
    String featureName = "featureName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    Integer startMonth = 56; // Integer | 
    Integer startYear = 56; // Integer | 
    try {
      ServiceDocsFeatureMonthlySummary result = apiInstance.v1DataFeatureMonthlySummaryGet(endMonth, endYear, featureName, pageSize, startKey, startMonth, startYear);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataApi#v1DataFeatureMonthlySummaryGet");
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
| **endMonth** | **Integer**|  | [optional] |
| **endYear** | **Integer**|  | [optional] |
| **featureName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **startMonth** | **Integer**|  | [optional] |
| **startYear** | **Integer**|  | [optional] |

### Return type

[**ServiceDocsFeatureMonthlySummary**](ServiceDocsFeatureMonthlySummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

