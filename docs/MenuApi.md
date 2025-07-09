# MenuApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDMenuGet**](MenuApi.md#v1AccountAccountIDMenuGet) | **GET** /v1/account/{accountID}/menu | Get Menu List |
| [**v1AccountAccountIDMenuMenuIDDelete**](MenuApi.md#v1AccountAccountIDMenuMenuIDDelete) | **DELETE** /v1/account/{accountID}/menu/{menuID} | Delete Menu |
| [**v1AccountAccountIDMenuMenuIDGet**](MenuApi.md#v1AccountAccountIDMenuMenuIDGet) | **GET** /v1/account/{accountID}/menu/{menuID} | Get Menu Details |
| [**v1AccountAccountIDMenuMenuIDPut**](MenuApi.md#v1AccountAccountIDMenuMenuIDPut) | **PUT** /v1/account/{accountID}/menu/{menuID} | Update Menu |
| [**v1AccountAccountIDMenuPost**](MenuApi.md#v1AccountAccountIDMenuPost) | **POST** /v1/account/{accountID}/menu | Create Menu |


<a id="v1AccountAccountIDMenuGet"></a>
# **v1AccountAccountIDMenuGet**
> MenuOutputList v1AccountAccountIDMenuGet(accountID, startKey, pageSize)

Get Menu List

Users can access data about all menus in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MenuApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MenuApi apiInstance = new MenuApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | start_key for pagination that was returned as next_start_key from your previous call
    Integer pageSize = 56; // Integer | number of records to return, range 1 to 50
    try {
      MenuOutputList result = apiInstance.v1AccountAccountIDMenuGet(accountID, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MenuApi#v1AccountAccountIDMenuGet");
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

[**MenuOutputList**](MenuOutputList.md)

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

<a id="v1AccountAccountIDMenuMenuIDDelete"></a>
# **v1AccountAccountIDMenuMenuIDDelete**
> MenuOutputDetail v1AccountAccountIDMenuMenuIDDelete(accountID, menuID)

Delete Menu

Delete a menu from an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MenuApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MenuApi apiInstance = new MenuApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String menuID = "menuID_example"; // String | Menu ID, 32 alpha numeric
    try {
      MenuOutputDetail result = apiInstance.v1AccountAccountIDMenuMenuIDDelete(accountID, menuID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MenuApi#v1AccountAccountIDMenuMenuIDDelete");
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
| **menuID** | **String**| Menu ID, 32 alpha numeric | |

### Return type

[**MenuOutputDetail**](MenuOutputDetail.md)

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

<a id="v1AccountAccountIDMenuMenuIDGet"></a>
# **v1AccountAccountIDMenuMenuIDGet**
> MenuOutputDetail v1AccountAccountIDMenuMenuIDGet(accountID, menuID)

Get Menu Details

Get details about a menu in an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MenuApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MenuApi apiInstance = new MenuApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String menuID = "menuID_example"; // String | Menu ID, 32 alpha numeric
    try {
      MenuOutputDetail result = apiInstance.v1AccountAccountIDMenuMenuIDGet(accountID, menuID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MenuApi#v1AccountAccountIDMenuMenuIDGet");
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
| **menuID** | **String**| Menu ID, 32 alpha numeric | |

### Return type

[**MenuOutputDetail**](MenuOutputDetail.md)

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

<a id="v1AccountAccountIDMenuMenuIDPut"></a>
# **v1AccountAccountIDMenuMenuIDPut**
> MenuOutputDetail v1AccountAccountIDMenuMenuIDPut(accountID, menuID, reqBody)

Update Menu

Edit an account menu.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MenuApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MenuApi apiInstance = new MenuApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String menuID = "menuID_example"; // String | Menu ID, 32 alpha numeric
    MenuInputData reqBody = new MenuInputData(); // MenuInputData | payload fields
    try {
      MenuOutputDetail result = apiInstance.v1AccountAccountIDMenuMenuIDPut(accountID, menuID, reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MenuApi#v1AccountAccountIDMenuMenuIDPut");
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
| **menuID** | **String**| Menu ID, 32 alpha numeric | |
| **reqBody** | [**MenuInputData**](MenuInputData.md)| payload fields | |

### Return type

[**MenuOutputDetail**](MenuOutputDetail.md)

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

<a id="v1AccountAccountIDMenuPost"></a>
# **v1AccountAccountIDMenuPost**
> MenuOutputDetail v1AccountAccountIDMenuPost(accountID, menu)

Create Menu

Create a new menu for an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MenuApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    MenuApi apiInstance = new MenuApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alphanumeric
    MenuInputData menu = new MenuInputData(); // MenuInputData | Menu data
    try {
      MenuOutputDetail result = apiInstance.v1AccountAccountIDMenuPost(accountID, menu);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MenuApi#v1AccountAccountIDMenuPost");
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
| **menu** | [**MenuInputData**](MenuInputData.md)| Menu data | |

### Return type

[**MenuOutputDetail**](MenuOutputDetail.md)

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

