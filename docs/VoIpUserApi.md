# VoIpUserApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountidUserGet**](VoIpUserApi.md#v1AccountAccountidUserGet) | **GET** /v1/account/{accountid}/user | Get User List |
| [**v1AccountAccountidUserPost**](VoIpUserApi.md#v1AccountAccountidUserPost) | **POST** /v1/account/{accountid}/user | Create User |
| [**v1AccountAccountidUserUseridDelete**](VoIpUserApi.md#v1AccountAccountidUserUseridDelete) | **DELETE** /v1/account/{accountid}/user/{userid} | Delete User |
| [**v1AccountAccountidUserUseridGet**](VoIpUserApi.md#v1AccountAccountidUserUseridGet) | **GET** /v1/account/{accountid}/user/{userid} | Get User Details |
| [**v1AccountAccountidUserUseridPut**](VoIpUserApi.md#v1AccountAccountidUserUseridPut) | **PUT** /v1/account/{accountid}/user/{userid} | Update User |
| [**v1AccountAccountidUserUseridUserauthPost**](VoIpUserApi.md#v1AccountAccountidUserUseridUserauthPost) | **POST** /v1/account/{accountid}/user/{userid}/userauth | Impersonate a User |


<a id="v1AccountAccountidUserGet"></a>
# **v1AccountAccountidUserGet**
> ServiceDocsUserGetAll v1AccountAccountidUserGet(accountid, startKey, pageSize)

Get User List

Get a list of all VoIP users that includes first and last names, email addresses, extensions, and account statuses.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      ServiceDocsUserGetAll result = apiInstance.v1AccountAccountidUserGet(accountid, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserGet");
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

[**ServiceDocsUserGetAll**](ServiceDocsUserGetAll.md)

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

<a id="v1AccountAccountidUserPost"></a>
# **v1AccountAccountidUserPost**
> ServiceDocsUserGetSingle v1AccountAccountidUserPost(accountid, user)

Create User

Add new users to the account. When a user is added, the system generates their unique 32 alpha numeric ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    ServiceVOIPUserAdd2 user = new ServiceVOIPUserAdd2(); // ServiceVOIPUserAdd2 | user fields
    try {
      ServiceDocsUserGetSingle result = apiInstance.v1AccountAccountidUserPost(accountid, user);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserPost");
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
| **user** | [**ServiceVOIPUserAdd2**](ServiceVOIPUserAdd2.md)| user fields | |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

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

<a id="v1AccountAccountidUserUseridDelete"></a>
# **v1AccountAccountidUserUseridDelete**
> ServiceDocsUserGetSingle v1AccountAccountidUserUseridDelete(accountid, userid)

Delete User

Delete VoIP user access to maintain the security of your accounts.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String userid = "userid_example"; // String | User ID, 32 alpha numeric
    try {
      ServiceDocsUserGetSingle result = apiInstance.v1AccountAccountidUserUseridDelete(accountid, userid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserUseridDelete");
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
| **userid** | **String**| User ID, 32 alpha numeric | |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

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

<a id="v1AccountAccountidUserUseridGet"></a>
# **v1AccountAccountidUserUseridGet**
> ServiceDocsUserGetSingle v1AccountAccountidUserUseridGet(accountid, userid)

Get User Details

View specific user details.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String userid = "userid_example"; // String | User ID, 32 alpha numeric
    try {
      ServiceDocsUserGetSingle result = apiInstance.v1AccountAccountidUserUseridGet(accountid, userid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserUseridGet");
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
| **userid** | **String**| User ID, 32 alpha numeric | |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

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

<a id="v1AccountAccountidUserUseridPut"></a>
# **v1AccountAccountidUserUseridPut**
> ServiceDocsUserGetSingle v1AccountAccountidUserUseridPut(accountid, userid, user)

Update User

Keep user information current. Modify the first and last name, extension, and other pertinent information.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String userid = "userid_example"; // String | User ID, 32 alpha numeric
    ServiceVOIPUserAdd2 user = new ServiceVOIPUserAdd2(); // ServiceVOIPUserAdd2 | user fields
    try {
      ServiceDocsUserGetSingle result = apiInstance.v1AccountAccountidUserUseridPut(accountid, userid, user);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserUseridPut");
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
| **userid** | **String**| User ID, 32 alpha numeric | |
| **user** | [**ServiceVOIPUserAdd2**](ServiceVOIPUserAdd2.md)| user fields | |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

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

<a id="v1AccountAccountidUserUseridUserauthPost"></a>
# **v1AccountAccountidUserUseridUserauthPost**
> ServiceDocsImpersonateUserGetSingle v1AccountAccountidUserUseridUserauthPost(accountid, userid, user)

Impersonate a User

Retrieve a token for making presence calls.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoIpUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    VoIpUserApi apiInstance = new VoIpUserApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String userid = "userid_example"; // String | User ID, 32 alpha numeric
    ServiceVOIPImpersonateUser user = new ServiceVOIPImpersonateUser(); // ServiceVOIPImpersonateUser | Payload for impersonate a user
    try {
      ServiceDocsImpersonateUserGetSingle result = apiInstance.v1AccountAccountidUserUseridUserauthPost(accountid, userid, user);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoIpUserApi#v1AccountAccountidUserUseridUserauthPost");
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
| **userid** | **String**| User ID, 32 alpha numeric | |
| **user** | [**ServiceVOIPImpersonateUser**](ServiceVOIPImpersonateUser.md)| Payload for impersonate a user | |

### Return type

[**ServiceDocsImpersonateUserGetSingle**](ServiceDocsImpersonateUserGetSingle.md)

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

