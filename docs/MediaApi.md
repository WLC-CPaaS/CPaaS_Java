# MediaApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDMediaMediaIDFileGet**](MediaApi.md#v1AccountAccountIDMediaMediaIDFileGet) | **GET** /v1/account/{accountID}/media/{mediaID}/file | Get Media File |
| [**v1AccountAccountIDMediaMediaIDFilePost**](MediaApi.md#v1AccountAccountIDMediaMediaIDFilePost) | **POST** /v1/account/{accountID}/media/{mediaID}/file | Add Media File |
| [**v1AccountAccountidMediaGet**](MediaApi.md#v1AccountAccountidMediaGet) | **GET** /v1/account/{accountid}/media | Get Media List |
| [**v1AccountAccountidMediaMediaidDelete**](MediaApi.md#v1AccountAccountidMediaMediaidDelete) | **DELETE** /v1/account/{accountid}/media/{mediaid} | Delete Media |
| [**v1AccountAccountidMediaMediaidGet**](MediaApi.md#v1AccountAccountidMediaMediaidGet) | **GET** /v1/account/{accountid}/media/{mediaid} | Get Media Details |
| [**v1AccountAccountidMediaPost**](MediaApi.md#v1AccountAccountidMediaPost) | **POST** /v1/account/{accountid}/media | Create Media |


<a id="v1AccountAccountIDMediaMediaIDFileGet"></a>
# **v1AccountAccountIDMediaMediaIDFileGet**
> File v1AccountAccountIDMediaMediaIDFileGet(accountID, mediaID)

Get Media File

Gather data about the media objects in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String mediaID = "mediaID_example"; // String | Media ID, 32 alpha numeric
    try {
      File result = apiInstance.v1AccountAccountIDMediaMediaIDFileGet(accountID, mediaID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountIDMediaMediaIDFileGet");
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
| **mediaID** | **String**| Media ID, 32 alpha numeric | |

### Return type

[**File**](File.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, audio/mp3, audio/mpeg, audio/mpeg3, audio/x-wav, audio/wav, audio/ogg, video/x-flv, video/h264, video/mpeg, video/quicktime, video/mp4, video/webm

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1AccountAccountIDMediaMediaIDFilePost"></a>
# **v1AccountAccountIDMediaMediaIDFilePost**
> ServiceDocsMediaGetSingle v1AccountAccountIDMediaMediaIDFilePost(accountID, mediaID, _file)

Add Media File

Include a media file that is connected to a media object in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String mediaID = "mediaID_example"; // String | Media ID, 32 alpha numeric
    File _file = new File("/path/to/file"); // File | Media file
    try {
      ServiceDocsMediaGetSingle result = apiInstance.v1AccountAccountIDMediaMediaIDFilePost(accountID, mediaID, _file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountIDMediaMediaIDFilePost");
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
| **mediaID** | **String**| Media ID, 32 alpha numeric | |
| **_file** | **File**| Media file | |

### Return type

[**ServiceDocsMediaGetSingle**](ServiceDocsMediaGetSingle.md)

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

<a id="v1AccountAccountidMediaGet"></a>
# **v1AccountAccountidMediaGet**
> ServiceDocsMediaGetAll v1AccountAccountidMediaGet(accountid, startKey, pageSize)

Get Media List

View all media files for an account in your organization.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsMediaGetAll result = apiInstance.v1AccountAccountidMediaGet(accountid, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountidMediaGet");
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
| **accountid** | **String**| Account ID, 32 alpha numeric | |
| **startKey** | **String**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **pageSize** | **Integer**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**ServiceDocsMediaGetAll**](ServiceDocsMediaGetAll.md)

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

<a id="v1AccountAccountidMediaMediaidDelete"></a>
# **v1AccountAccountidMediaMediaidDelete**
> ServiceDocsMediaGetSingle v1AccountAccountidMediaMediaidDelete(accountid, mediaid)

Delete Media

Remove a media file that is no longer in use from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String mediaid = "mediaid_example"; // String | Device ID, 32 alpha numeric
    try {
      ServiceDocsMediaGetSingle result = apiInstance.v1AccountAccountidMediaMediaidDelete(accountid, mediaid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountidMediaMediaidDelete");
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
| **accountid** | **String**| Account ID, 32 alpha numeric | |
| **mediaid** | **String**| Device ID, 32 alpha numeric | |

### Return type

[**ServiceDocsMediaGetSingle**](ServiceDocsMediaGetSingle.md)

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

<a id="v1AccountAccountidMediaMediaidGet"></a>
# **v1AccountAccountidMediaMediaidGet**
> ServiceDocsMediaGetSingle v1AccountAccountidMediaMediaidGet(accountid, mediaid)

Get Media Details

Permit users to view an account&#39;s specific media information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String mediaid = "mediaid_example"; // String | Media ID, 32 alpha numeric
    try {
      ServiceDocsMediaGetSingle result = apiInstance.v1AccountAccountidMediaMediaidGet(accountid, mediaid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountidMediaMediaidGet");
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
| **accountid** | **String**| Account ID, 32 alpha numeric | |
| **mediaid** | **String**| Media ID, 32 alpha numeric | |

### Return type

[**ServiceDocsMediaGetSingle**](ServiceDocsMediaGetSingle.md)

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

<a id="v1AccountAccountidMediaPost"></a>
# **v1AccountAccountidMediaPost**
> ServiceDocsMediaGetSingle v1AccountAccountidMediaPost(accountid, media)

Create Media

Generate a media object to allow users to upload a media file in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPMediaAddEditData media = new ServiceVOIPMediaAddEditData(); // ServiceVOIPMediaAddEditData | Media creation or update payload
    try {
      ServiceDocsMediaGetSingle result = apiInstance.v1AccountAccountidMediaPost(accountid, media);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#v1AccountAccountidMediaPost");
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
| **accountid** | **String**| Account ID, 32 alpha numeric | |
| **media** | [**ServiceVOIPMediaAddEditData**](ServiceVOIPMediaAddEditData.md)| Media creation or update payload | |

### Return type

[**ServiceDocsMediaGetSingle**](ServiceDocsMediaGetSingle.md)

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

