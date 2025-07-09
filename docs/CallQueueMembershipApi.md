# CallQueueMembershipApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDQueuemembershipPost**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipPost) | **POST** /v1/account/{accountID}/queuemembership | Grant Queue Membership to User |
| [**v1AccountAccountIDQueuemembershipRecipientIDDisablePost**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipRecipientIDDisablePost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/disable | Disable Queue Membership |
| [**v1AccountAccountIDQueuemembershipRecipientIDEnablePost**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipRecipientIDEnablePost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/enable | Enable Queue Membership |


<a id="v1AccountAccountIDQueuemembershipPost"></a>
# **v1AccountAccountIDQueuemembershipPost**
> ServiceDocsQueueMembershipOutput v1AccountAccountIDQueuemembershipPost(accountID, reqBody)

Grant Queue Membership to User

Allow users to create queue memberships for recipients.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueMembershipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueMembershipApi apiInstance = new CallQueueMembershipApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPQueueMembershipAddData reqBody = new ServiceVOIPQueueMembershipAddData(); // ServiceVOIPQueueMembershipAddData | payload fields
    try {
      ServiceDocsQueueMembershipOutput result = apiInstance.v1AccountAccountIDQueuemembershipPost(accountID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueMembershipApi#v1AccountAccountIDQueuemembershipPost");
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
| **reqBody** | [**ServiceVOIPQueueMembershipAddData**](ServiceVOIPQueueMembershipAddData.md)| payload fields | |

### Return type

[**ServiceDocsQueueMembershipOutput**](ServiceDocsQueueMembershipOutput.md)

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

<a id="v1AccountAccountIDQueuemembershipRecipientIDDisablePost"></a>
# **v1AccountAccountIDQueuemembershipRecipientIDDisablePost**
> ServiceAPIResponse v1AccountAccountIDQueuemembershipRecipientIDDisablePost(accountID, recipientID)

Disable Queue Membership

Deactivate queue membership for a recipient.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueMembershipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueMembershipApi apiInstance = new CallQueueMembershipApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String recipientID = "recipientID_example"; // String | Recipient ID, 32 alpha numeric
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDQueuemembershipRecipientIDDisablePost(accountID, recipientID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueMembershipApi#v1AccountAccountIDQueuemembershipRecipientIDDisablePost");
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
| **recipientID** | **String**| Recipient ID, 32 alpha numeric | |

### Return type

[**ServiceAPIResponse**](ServiceAPIResponse.md)

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

<a id="v1AccountAccountIDQueuemembershipRecipientIDEnablePost"></a>
# **v1AccountAccountIDQueuemembershipRecipientIDEnablePost**
> ServiceAPIResponse v1AccountAccountIDQueuemembershipRecipientIDEnablePost(accountID, recipientID, reqBody)

Enable Queue Membership

Activate queue membership for a recipient.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CallQueueMembershipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CallQueueMembershipApi apiInstance = new CallQueueMembershipApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String recipientID = "recipientID_example"; // String | Recipient ID, 32 alpha numeric
    ServiceVOIPCallQueueEnableMembershipData reqBody = new ServiceVOIPCallQueueEnableMembershipData(); // ServiceVOIPCallQueueEnableMembershipData | payload fields
    try {
      ServiceAPIResponse result = apiInstance.v1AccountAccountIDQueuemembershipRecipientIDEnablePost(accountID, recipientID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CallQueueMembershipApi#v1AccountAccountIDQueuemembershipRecipientIDEnablePost");
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
| **recipientID** | **String**| Recipient ID, 32 alpha numeric | |
| **reqBody** | [**ServiceVOIPCallQueueEnableMembershipData**](ServiceVOIPCallQueueEnableMembershipData.md)| payload fields | |

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

