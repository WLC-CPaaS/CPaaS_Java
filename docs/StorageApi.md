# StorageApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDStorageDelete**](StorageApi.md#v1AccountAccountIDStorageDelete) | **DELETE** /v1/account/{accountID}/storage | Delete Storage |
| [**v1AccountAccountIDStorageGet**](StorageApi.md#v1AccountAccountIDStorageGet) | **GET** /v1/account/{accountID}/storage | Get Storage Details |
| [**v1AccountAccountIDStoragePost**](StorageApi.md#v1AccountAccountIDStoragePost) | **POST** /v1/account/{accountID}/storage | Create Storage |
| [**v1AccountAccountIDStoragePut**](StorageApi.md#v1AccountAccountIDStoragePut) | **PUT** /v1/account/{accountID}/storage | Update Storage |


<a id="v1AccountAccountIDStorageDelete"></a>
# **v1AccountAccountIDStorageDelete**
> ServiceDocsStorageGet v1AccountAccountIDStorageDelete(accountID)

Delete Storage

Delete items that are stored in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsStorageGet result = apiInstance.v1AccountAccountIDStorageDelete(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#v1AccountAccountIDStorageDelete");
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

[**ServiceDocsStorageGet**](ServiceDocsStorageGet.md)

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

<a id="v1AccountAccountIDStorageGet"></a>
# **v1AccountAccountIDStorageGet**
> ServiceDocsStorageGet v1AccountAccountIDStorageGet(accountID)

Get Storage Details

Retrieve storage details for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    try {
      ServiceDocsStorageGet result = apiInstance.v1AccountAccountIDStorageGet(accountID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#v1AccountAccountIDStorageGet");
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

[**ServiceDocsStorageGet**](ServiceDocsStorageGet.md)

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

<a id="v1AccountAccountIDStoragePost"></a>
# **v1AccountAccountIDStoragePost**
> ServiceDocsStorageGet v1AccountAccountIDStoragePost(accountID, reqBody)

Create Storage

Create storage in an account for voicemails, call recordings, faxes, etc.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPStorageAddEditData reqBody = new ServiceVOIPStorageAddEditData(); // ServiceVOIPStorageAddEditData | payload fields
    try {
      ServiceDocsStorageGet result = apiInstance.v1AccountAccountIDStoragePost(accountID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#v1AccountAccountIDStoragePost");
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
| **reqBody** | [**ServiceVOIPStorageAddEditData**](ServiceVOIPStorageAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsStorageGet**](ServiceDocsStorageGet.md)

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

<a id="v1AccountAccountIDStoragePut"></a>
# **v1AccountAccountIDStoragePut**
> ServiceDocsStorageGet v1AccountAccountIDStoragePut(accountID, reqBody)

Update Storage

Modify the names of metadata to make it easier to locate (e.g., change the name of voicemail_storage to voicemail_and_callrecordings_storage, etc.).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPStorageAddEditData reqBody = new ServiceVOIPStorageAddEditData(); // ServiceVOIPStorageAddEditData | payload fields
    try {
      ServiceDocsStorageGet result = apiInstance.v1AccountAccountIDStoragePut(accountID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#v1AccountAccountIDStoragePut");
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
| **reqBody** | [**ServiceVOIPStorageAddEditData**](ServiceVOIPStorageAddEditData.md)| payload fields | |

### Return type

[**ServiceDocsStorageGet**](ServiceDocsStorageGet.md)

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

