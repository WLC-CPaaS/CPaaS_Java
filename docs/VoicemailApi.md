# VoicemailApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDVoicemailGet**](VoicemailApi.md#v1AccountAccountIDVoicemailGet) | **GET** /v1/account/{accountID}/voicemail | Get Voicemail Box List |
| [**v1AccountAccountIDVoicemailPost**](VoicemailApi.md#v1AccountAccountIDVoicemailPost) | **POST** /v1/account/{accountID}/voicemail | Create Voicemail Box |
| [**v1AccountAccountIDVoicemailVoicemailIDDelete**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDDelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID} | Delete Voicemail Box |
| [**v1AccountAccountIDVoicemailVoicemailIDGet**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID} | Get Voicemail Box Details |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageGet**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message | Get Voicemail Message List |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Delete Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Get Voicemail Message Details |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Update Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Get Voicemail Message File |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Add Voicemail Message File |
| [**v1AccountAccountIDVoicemailVoicemailIDMessagePost**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessagePost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message | Create Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDPut**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDPut) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID} | Update Voicemail Box |


<a id="v1AccountAccountIDVoicemailGet"></a>
# **v1AccountAccountIDVoicemailGet**
> ServiceDocsVoicemailGetAll v1AccountAccountIDVoicemailGet(accountID, startKey, pageSize)

Get Voicemail Box List

List all voicemail boxes in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsVoicemailGetAll result = apiInstance.v1AccountAccountIDVoicemailGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailGet");
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

[**ServiceDocsVoicemailGetAll**](ServiceDocsVoicemailGetAll.md)

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

<a id="v1AccountAccountIDVoicemailPost"></a>
# **v1AccountAccountIDVoicemailPost**
> ServiceDocsVoicemailGetSingle v1AccountAccountIDVoicemailPost(accountID, voicemail)

Create Voicemail Box

Create a voicemail box for receiving and storing voicemail messages.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | account ID, 32 alphanumeric
    ServiceVOIPVoicemailAddEditData voicemail = new ServiceVOIPVoicemailAddEditData(); // ServiceVOIPVoicemailAddEditData | voicemail payload fields
    try {
      ServiceDocsVoicemailGetSingle result = apiInstance.v1AccountAccountIDVoicemailPost(accountID, voicemail);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailPost");
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
| **accountID** | **String**| account ID, 32 alphanumeric | |
| **voicemail** | [**ServiceVOIPVoicemailAddEditData**](ServiceVOIPVoicemailAddEditData.md)| voicemail payload fields | |

### Return type

[**ServiceDocsVoicemailGetSingle**](ServiceDocsVoicemailGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDDelete"></a>
# **v1AccountAccountIDVoicemailVoicemailIDDelete**
> ServiceDocsVoicemailGetSingle v1AccountAccountIDVoicemailVoicemailIDDelete(accountID, voicemailID)

Delete Voicemail Box

Delete a voicemail box in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    try {
      ServiceDocsVoicemailGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDDelete(accountID, voicemailID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDDelete");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |

### Return type

[**ServiceDocsVoicemailGetSingle**](ServiceDocsVoicemailGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDGet"></a>
# **v1AccountAccountIDVoicemailVoicemailIDGet**
> ServiceDocsVoicemailGetSingle v1AccountAccountIDVoicemailVoicemailIDGet(accountID, voicemailID)

Get Voicemail Box Details

Get information about a single voicemail box.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    try {
      ServiceDocsVoicemailGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDGet(accountID, voicemailID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDGet");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |

### Return type

[**ServiceDocsVoicemailGetSingle**](ServiceDocsVoicemailGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageGet"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageGet**
> ServiceDocsVoicemailMessageGetAll v1AccountAccountIDVoicemailVoicemailIDMessageGet(accountID, voicemailID, startKey, pageSize)

Get Voicemail Message List

Get a list of voicemail messages from an account&#39;s voicemail box.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | voicemail ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsVoicemailMessageGetAll result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageGet(accountID, voicemailID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageGet");
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
| **voicemailID** | **String**| voicemail ID, 32 alpha numeric | |
| **startKey** | **String**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **pageSize** | **Integer**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**ServiceDocsVoicemailMessageGetAll**](ServiceDocsVoicemailMessageGetAll.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete**
> ServiceDocsVoicemailMessageGetSingle v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete(accountID, voicemailID, messageID)

Delete Voicemail Message

Delete a voicemail message from a voicemail box in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    String messageID = "messageID_example"; // String | message ID, 32 alpha numeric
    try {
      ServiceDocsVoicemailMessageGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete(accountID, voicemailID, messageID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |
| **messageID** | **String**| message ID, 32 alpha numeric | |

### Return type

[**ServiceDocsVoicemailMessageGetSingle**](ServiceDocsVoicemailMessageGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet**
> ServiceDocsVoicemailMessageGetSingle v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet(accountID, voicemailID, messageID)

Get Voicemail Message Details

Retrieve the container details of an individual voicemail message. This includes a reference to the audio file, but not the message itself.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    String messageID = "messageID_example"; // String | Message ID, 39 (yyyymm-<32 id>)
    try {
      ServiceDocsVoicemailMessageGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet(accountID, voicemailID, messageID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |
| **messageID** | **String**| Message ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**ServiceDocsVoicemailMessageGetSingle**](ServiceDocsVoicemailMessageGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut**
> ServiceDocsVoicemailMessageGetSingle v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut(accountID, voicemailID, messageID, reqBody)

Update Voicemail Message

Copy or move a voicemail message to a different folder in the same voicemail box or move the message to a separate voicemail box.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    String messageID = "messageID_example"; // String | Message ID, 39 (yyyymm-<32 id>)
    ServiceVOIPVoicemailMessageChange reqBody = new ServiceVOIPVoicemailMessageChange(); // ServiceVOIPVoicemailMessageChange | payload fields
    try {
      ServiceDocsVoicemailMessageGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut(accountID, voicemailID, messageID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |
| **messageID** | **String**| Message ID, 39 (yyyymm-&lt;32 id&gt;) | |
| **reqBody** | [**ServiceVOIPVoicemailMessageChange**](ServiceVOIPVoicemailMessageChange.md)| payload fields | |

### Return type

[**ServiceDocsVoicemailMessageGetSingle**](ServiceDocsVoicemailMessageGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet**
> File v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet(accountID, voicemailID, messageID)

Get Voicemail Message File

Get the original audio content of a specific voicemail message identified by its unique ID within an account&#39;s voicemail box. URL Param \&quot;voicemailID\&quot; is a unique 32-character alphanumeric identifier assigned by the system, which refers to a specific voicemail box. URL Param \&quot;messageID\&quot; is a unique 32-character alphanumeric identifier assigned by the system, which refers to a specific message within a voicemail box.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, unique 32-character alphanumeric identifier
    String voicemailID = "voicemailID_example"; // String | Voicemail Box ID, unique 32-character alphanumeric identifier
    String messageID = "messageID_example"; // String | Message ID, unique 32-character alphanumeric identifier
    try {
      File result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet(accountID, voicemailID, messageID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet");
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
| **accountID** | **String**| Account ID, unique 32-character alphanumeric identifier | |
| **voicemailID** | **String**| Voicemail Box ID, unique 32-character alphanumeric identifier | |
| **messageID** | **String**| Message ID, unique 32-character alphanumeric identifier | |

### Return type

[**File**](File.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost**
> Map&lt;String, Object&gt; v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost(accountID, voicemailID, messageID, _file)

Add Voicemail Message File

Associate an audio recording file with the voicemail to fully complete the message.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alphanumeric characters
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alphanumeric characters
    String messageID = "messageID_example"; // String | Message ID, 32 alphanumeric characters
    File _file = new File("/path/to/file"); // File | Audio file to upload
    try {
      Map<String, Object> result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost(accountID, voicemailID, messageID, _file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost");
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
| **accountID** | **String**| Account ID, 32 alphanumeric characters | |
| **voicemailID** | **String**| Voicemail ID, 32 alphanumeric characters | |
| **messageID** | **String**| Message ID, 32 alphanumeric characters | |
| **_file** | **File**| Audio file to upload | |

### Return type

**Map&lt;String, Object&gt;**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDVoicemailVoicemailIDMessagePost"></a>
# **v1AccountAccountIDVoicemailVoicemailIDMessagePost**
> ServiceDocsVoicemailMessageGetSingle v1AccountAccountIDVoicemailVoicemailIDMessagePost(accountID, voicemailID, message)

Create Voicemail Message

Create the container information for a recorded voicemail message in a voicemail box.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | account ID, 32 alphanumeric
    String voicemailID = "voicemailID_example"; // String | voicemail ID, 32 alphanumeric
    ServiceVOIPVoicemailMessageAddData message = new ServiceVOIPVoicemailMessageAddData(); // ServiceVOIPVoicemailMessageAddData | voicemail message payload fields
    try {
      ServiceDocsVoicemailMessageGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDMessagePost(accountID, voicemailID, message);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDMessagePost");
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
| **accountID** | **String**| account ID, 32 alphanumeric | |
| **voicemailID** | **String**| voicemail ID, 32 alphanumeric | |
| **message** | [**ServiceVOIPVoicemailMessageAddData**](ServiceVOIPVoicemailMessageAddData.md)| voicemail message payload fields | |

### Return type

[**ServiceDocsVoicemailMessageGetSingle**](ServiceDocsVoicemailMessageGetSingle.md)

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

<a id="v1AccountAccountIDVoicemailVoicemailIDPut"></a>
# **v1AccountAccountIDVoicemailVoicemailIDPut**
> ServiceDocsVoicemailGetSingle v1AccountAccountIDVoicemailVoicemailIDPut(accountID, voicemailID, reqBody)

Update Voicemail Box

Update the settings in an individual voicemail box, such as the owner, PIN, etc.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoicemailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoicemailApi apiInstance = new VoicemailApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String voicemailID = "voicemailID_example"; // String | Voicemail ID, 32 alpha numeric
    ServiceVOIPVoicemailAddEditData reqBody = new ServiceVOIPVoicemailAddEditData(); // ServiceVOIPVoicemailAddEditData | payload fields
    try {
      ServiceDocsVoicemailGetSingle result = apiInstance.v1AccountAccountIDVoicemailVoicemailIDPut(accountID, voicemailID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoicemailApi#v1AccountAccountIDVoicemailVoicemailIDPut");
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
| **voicemailID** | **String**| Voicemail ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPVoicemailAddEditData**](ServiceVOIPVoicemailAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsVoicemailGetSingle**](ServiceDocsVoicemailGetSingle.md)

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

