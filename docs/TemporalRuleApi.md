# TemporalRuleApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDTemporalruleGet**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleGet) | **GET** /v1/account/{accountID}/temporalrule | Get Temporal Rule List |
| [**v1AccountAccountIDTemporalrulePost**](TemporalRuleApi.md#v1AccountAccountIDTemporalrulePost) | **POST** /v1/account/{accountID}/temporalrule | Create Temporal Rule |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDDelete**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDDelete) | **DELETE** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Delete Temporal Rule |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDGet**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDGet) | **GET** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Get Temporal Rule Details |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDPut**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDPut) | **PUT** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Update Temporal Rule |


<a id="v1AccountAccountIDTemporalruleGet"></a>
# **v1AccountAccountIDTemporalruleGet**
> ServiceDocsTemporalRuleGetAll v1AccountAccountIDTemporalruleGet(accountID, startKey, pageSize)

Get Temporal Rule List

Access all temporal rules for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleApi apiInstance = new TemporalRuleApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsTemporalRuleGetAll result = apiInstance.v1AccountAccountIDTemporalruleGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleApi#v1AccountAccountIDTemporalruleGet");
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

[**ServiceDocsTemporalRuleGetAll**](ServiceDocsTemporalRuleGetAll.md)

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

<a id="v1AccountAccountIDTemporalrulePost"></a>
# **v1AccountAccountIDTemporalrulePost**
> ServiceDocsTemporalRuleGetSingle v1AccountAccountIDTemporalrulePost(accountID, temporalrule)

Create Temporal Rule

Create temporal rules for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleApi apiInstance = new TemporalRuleApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alphanumeric
    ServiceVOIPTemporalRuleAddEdit2 temporalrule = new ServiceVOIPTemporalRuleAddEdit2(); // ServiceVOIPTemporalRuleAddEdit2 | payload fields
    try {
      ServiceDocsTemporalRuleGetSingle result = apiInstance.v1AccountAccountIDTemporalrulePost(accountID, temporalrule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleApi#v1AccountAccountIDTemporalrulePost");
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
| **temporalrule** | [**ServiceVOIPTemporalRuleAddEdit2**](ServiceVOIPTemporalRuleAddEdit2.md)| payload fields | |

### Return type

[**ServiceDocsTemporalRuleGetSingle**](ServiceDocsTemporalRuleGetSingle.md)

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

<a id="v1AccountAccountIDTemporalruleTemporalRuleIDDelete"></a>
# **v1AccountAccountIDTemporalruleTemporalRuleIDDelete**
> ServiceDocsTemporalRuleGetSingle v1AccountAccountIDTemporalruleTemporalRuleIDDelete(accountID, temporalRuleID)

Delete Temporal Rule

Remove a temporal rule from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleApi apiInstance = new TemporalRuleApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleID = "temporalRuleID_example"; // String | temporal rule ID, 32 alpha numeric
    try {
      ServiceDocsTemporalRuleGetSingle result = apiInstance.v1AccountAccountIDTemporalruleTemporalRuleIDDelete(accountID, temporalRuleID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleApi#v1AccountAccountIDTemporalruleTemporalRuleIDDelete");
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
| **temporalRuleID** | **String**| temporal rule ID, 32 alpha numeric | |

### Return type

[**ServiceDocsTemporalRuleGetSingle**](ServiceDocsTemporalRuleGetSingle.md)

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

<a id="v1AccountAccountIDTemporalruleTemporalRuleIDGet"></a>
# **v1AccountAccountIDTemporalruleTemporalRuleIDGet**
> ServiceDocsTemporalRuleGetSingle v1AccountAccountIDTemporalruleTemporalRuleIDGet(accountID, temporalRuleID)

Get Temporal Rule Details

View details about individual time rules.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleApi apiInstance = new TemporalRuleApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleID = "temporalRuleID_example"; // String | Temporal Rule ID, 32 alpha numeric
    try {
      ServiceDocsTemporalRuleGetSingle result = apiInstance.v1AccountAccountIDTemporalruleTemporalRuleIDGet(accountID, temporalRuleID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleApi#v1AccountAccountIDTemporalruleTemporalRuleIDGet");
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
| **temporalRuleID** | **String**| Temporal Rule ID, 32 alpha numeric | |

### Return type

[**ServiceDocsTemporalRuleGetSingle**](ServiceDocsTemporalRuleGetSingle.md)

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

<a id="v1AccountAccountIDTemporalruleTemporalRuleIDPut"></a>
# **v1AccountAccountIDTemporalruleTemporalRuleIDPut**
> ServiceDocsTemporalRuleGetSingle v1AccountAccountIDTemporalruleTemporalRuleIDPut(accountID, temporalRuleID, reqBody)

Update Temporal Rule

Edit the existing temporal rules in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemporalRuleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    TemporalRuleApi apiInstance = new TemporalRuleApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String temporalRuleID = "temporalRuleID_example"; // String | Temporal Rule ID, 32 alpha numeric
    ServiceVOIPTemporalRuleAddEdit2 reqBody = new ServiceVOIPTemporalRuleAddEdit2(); // ServiceVOIPTemporalRuleAddEdit2 | payload fields
    try {
      ServiceDocsTemporalRuleGetSingle result = apiInstance.v1AccountAccountIDTemporalruleTemporalRuleIDPut(accountID, temporalRuleID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemporalRuleApi#v1AccountAccountIDTemporalruleTemporalRuleIDPut");
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
| **temporalRuleID** | **String**| Temporal Rule ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPTemporalRuleAddEdit2**](ServiceVOIPTemporalRuleAddEdit2.md)| payload fields | |

### Return type

[**ServiceDocsTemporalRuleGetSingle**](ServiceDocsTemporalRuleGetSingle.md)

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

