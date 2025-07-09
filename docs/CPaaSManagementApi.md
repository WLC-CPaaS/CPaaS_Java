# CPaaSManagementApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1MgmtUserGet**](CPaaSManagementApi.md#v1MgmtUserGet) | **GET** /v1/mgmt/user | Get All CPaaS Users |
| [**v1MgmtUserPost**](CPaaSManagementApi.md#v1MgmtUserPost) | **POST** /v1/mgmt/user | Invite CPaaS User |
| [**v1MgmtUserUserIDDelete**](CPaaSManagementApi.md#v1MgmtUserUserIDDelete) | **DELETE** /v1/mgmt/user/{userID} | Delete CPaaS User |
| [**v1MgmtUserUserIDGet**](CPaaSManagementApi.md#v1MgmtUserUserIDGet) | **GET** /v1/mgmt/user/{userID} | Get CPaaS User Details |
| [**v1MgmtUserUserIDPut**](CPaaSManagementApi.md#v1MgmtUserUserIDPut) | **PUT** /v1/mgmt/user/{userID} | Update CPaaS User Role |


<a id="v1MgmtUserGet"></a>
# **v1MgmtUserGet**
> ServiceDocsAdminUserGetAll v1MgmtUserGet(pageSize, startKey, sort, email, role, firstName, lastName)

Get All CPaaS Users

Retrieve a list of all CPaaS users in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CPaaSManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CPaaSManagementApi apiInstance = new CPaaSManagementApi(defaultClient);
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 100
    String startKey = "startKey_example"; // String | unique to fetch next records
    String sort = "sort_example"; // String | sorting the records by email(default)/role/first_name/last_name, _A is for ascending and _D is for descending, eg: sort=role_A,email_D
    String email = "email_example"; // String | Email
    String role = "role_example"; // String | User Role
    String firstName = "firstName_example"; // String | First Name
    String lastName = "lastName_example"; // String | Last Name
    try {
      ServiceDocsAdminUserGetAll result = apiInstance.v1MgmtUserGet(pageSize, startKey, sort, email, role, firstName, lastName);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CPaaSManagementApi#v1MgmtUserGet");
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
| **pageSize** | **Integer**| number of records to return, range 1 to 100 | [optional] |
| **startKey** | **String**| unique to fetch next records | [optional] |
| **sort** | **String**| sorting the records by email(default)/role/first_name/last_name, _A is for ascending and _D is for descending, eg: sort&#x3D;role_A,email_D | [optional] |
| **email** | **String**| Email | [optional] |
| **role** | **String**| User Role | [optional] |
| **firstName** | **String**| First Name | [optional] |
| **lastName** | **String**| Last Name | [optional] |

### Return type

[**ServiceDocsAdminUserGetAll**](ServiceDocsAdminUserGetAll.md)

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

<a id="v1MgmtUserPost"></a>
# **v1MgmtUserPost**
> ServiceDocsAdminUserGetSingle v1MgmtUserPost(reqBody)

Invite CPaaS User

Link a new CPaaS user to an existing client account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CPaaSManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CPaaSManagementApi apiInstance = new CPaaSManagementApi(defaultClient);
    ServiceAdminUserAddData reqBody = new ServiceAdminUserAddData(); // ServiceAdminUserAddData | payload fields
    try {
      ServiceDocsAdminUserGetSingle result = apiInstance.v1MgmtUserPost(reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CPaaSManagementApi#v1MgmtUserPost");
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
| **reqBody** | [**ServiceAdminUserAddData**](ServiceAdminUserAddData.md)| payload fields | |

### Return type

[**ServiceDocsAdminUserGetSingle**](ServiceDocsAdminUserGetSingle.md)

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

<a id="v1MgmtUserUserIDDelete"></a>
# **v1MgmtUserUserIDDelete**
> ServiceDocsAdminUserDelete v1MgmtUserUserIDDelete(userID)

Delete CPaaS User

Delete a CPaaS user from the associated account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CPaaSManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CPaaSManagementApi apiInstance = new CPaaSManagementApi(defaultClient);
    String userID = "userID_example"; // String | User ID, numeric
    try {
      ServiceDocsAdminUserDelete result = apiInstance.v1MgmtUserUserIDDelete(userID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CPaaSManagementApi#v1MgmtUserUserIDDelete");
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
| **userID** | **String**| User ID, numeric | |

### Return type

[**ServiceDocsAdminUserDelete**](ServiceDocsAdminUserDelete.md)

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

<a id="v1MgmtUserUserIDGet"></a>
# **v1MgmtUserUserIDGet**
> ServiceDocsAdminUserGetSingle v1MgmtUserUserIDGet(userID)

Get CPaaS User Details

View details about each CPaaS user in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CPaaSManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CPaaSManagementApi apiInstance = new CPaaSManagementApi(defaultClient);
    String userID = "userID_example"; // String | User ID, numeric
    try {
      ServiceDocsAdminUserGetSingle result = apiInstance.v1MgmtUserUserIDGet(userID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CPaaSManagementApi#v1MgmtUserUserIDGet");
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
| **userID** | **String**| User ID, numeric | |

### Return type

[**ServiceDocsAdminUserGetSingle**](ServiceDocsAdminUserGetSingle.md)

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

<a id="v1MgmtUserUserIDPut"></a>
# **v1MgmtUserUserIDPut**
> ServiceDocsAdminUserGetSingle v1MgmtUserUserIDPut(userID, reqBody)

Update CPaaS User Role

Update a CPaaS user&#39;s role within a client&#39;s account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.CPaaSManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    CPaaSManagementApi apiInstance = new CPaaSManagementApi(defaultClient);
    String userID = "userID_example"; // String | User ID, numeric
    ServiceAdminUserEditData reqBody = new ServiceAdminUserEditData(); // ServiceAdminUserEditData | payload fields
    try {
      ServiceDocsAdminUserGetSingle result = apiInstance.v1MgmtUserUserIDPut(userID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CPaaSManagementApi#v1MgmtUserUserIDPut");
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
| **userID** | **String**| User ID, numeric | |
| **reqBody** | [**ServiceAdminUserEditData**](ServiceAdminUserEditData.md)| payload fields | |

### Return type

[**ServiceDocsAdminUserGetSingle**](ServiceDocsAdminUserGetSingle.md)

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

