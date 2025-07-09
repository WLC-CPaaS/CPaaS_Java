# TemporalRuleSetApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDTemporalrulesetGet**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetGet) | **GET** /v1/account/{accountID}/temporalruleset | Get Temporal Rule Set List |
| [**v1AccountAccountIDTemporalrulesetPost**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetPost) | **POST** /v1/account/{accountID}/temporalruleset | Create Temporal Rule Set |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete) | **DELETE** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Delete Temporal Rule Set |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet) | **GET** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Get Temporal Rule Set Details |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut) | **PUT** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Update Temporal Rule Set |


<a id="v1AccountAccountIDTemporalrulesetGet"></a>
# **v1AccountAccountIDTemporalrulesetGet**
> ServiceDocsTemporalRuleSetGetAll v1AccountAccountIDTemporalrulesetGet(accountID, startKey, pageSize)

Get Temporal Rule Set List

Access the temporal rule set list in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleSetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleSetApi apiInstance = new TemporalRuleSetApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsTemporalRuleSetGetAll result = apiInstance.v1AccountAccountIDTemporalrulesetGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleSetApi#v1AccountAccountIDTemporalrulesetGet");
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

[**ServiceDocsTemporalRuleSetGetAll**](ServiceDocsTemporalRuleSetGetAll.md)

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

<a id="v1AccountAccountIDTemporalrulesetPost"></a>
# **v1AccountAccountIDTemporalrulesetPost**
> ServiceDocsTemporalRuleSetGetSingle v1AccountAccountIDTemporalrulesetPost(accountID, temporalruleset)

Create Temporal Rule Set

Develop a new temporal rule set for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleSetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleSetApi apiInstance = new TemporalRuleSetApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alphanumeric
    ServiceVOIPTemporalRuleSetAddEditData temporalruleset = new ServiceVOIPTemporalRuleSetAddEditData(); // ServiceVOIPTemporalRuleSetAddEditData | payload fields
    try {
      ServiceDocsTemporalRuleSetGetSingle result = apiInstance.v1AccountAccountIDTemporalrulesetPost(accountID, temporalruleset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleSetApi#v1AccountAccountIDTemporalrulesetPost");
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
| **accountID** | **String**| Account ID, 32 alphanumeric | |
| **temporalruleset** | [**ServiceVOIPTemporalRuleSetAddEditData**](ServiceVOIPTemporalRuleSetAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

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

<a id="v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete"></a>
# **v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete**
> ServiceDocsTemporalRuleSetGetSingle v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete(accountID, temporalRuleSetID)

Delete Temporal Rule Set

Delete the temporal rule set from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleSetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleSetApi apiInstance = new TemporalRuleSetApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleSetID = "temporalRuleSetID_example"; // String | temporal rule set ID, 32 alpha numeric
    try {
      ServiceDocsTemporalRuleSetGetSingle result = apiInstance.v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete(accountID, temporalRuleSetID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleSetApi#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete");
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
| **temporalRuleSetID** | **String**| temporal rule set ID, 32 alpha numeric | |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

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

<a id="v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet"></a>
# **v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet**
> ServiceDocsTemporalRuleSetGetSingle v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet(accountID, temporalRuleSetID)

Get Temporal Rule Set Details

Acquire details about a temporal rule set in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleSetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleSetApi apiInstance = new TemporalRuleSetApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleSetID = "temporalRuleSetID_example"; // String | Temporal Ruleset ID, 32 alpha numeric
    try {
      ServiceDocsTemporalRuleSetGetSingle result = apiInstance.v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet(accountID, temporalRuleSetID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleSetApi#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet");
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
| **temporalRuleSetID** | **String**| Temporal Ruleset ID, 32 alpha numeric | |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

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

<a id="v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut"></a>
# **v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut**
> ServiceDocsTemporalRuleSetGetSingle v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut(accountID, temporalRuleSetID, reqBody)

Update Temporal Rule Set

Efficiently adjust the temporal rule set in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleSetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleSetApi apiInstance = new TemporalRuleSetApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleSetID = "temporalRuleSetID_example"; // String | Temporal Ruleset ID, 32 alpha numeric
    ServiceVOIPTemporalRuleSetAddEditData reqBody = new ServiceVOIPTemporalRuleSetAddEditData(); // ServiceVOIPTemporalRuleSetAddEditData | payload fields
    try {
      ServiceDocsTemporalRuleSetGetSingle result = apiInstance.v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut(accountID, temporalRuleSetID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleSetApi#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut");
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
| **temporalRuleSetID** | **String**| Temporal Ruleset ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPTemporalRuleSetAddEditData**](ServiceVOIPTemporalRuleSetAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

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

