# PhoneNumberApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountidPhonenumberGet**](PhoneNumberApi.md#v1AccountAccountidPhonenumberGet) | **GET** /v1/account/{accountid}/phonenumber | Get Assigned Numbers List |
| [**v1AccountPhonenumberAssignPost**](PhoneNumberApi.md#v1AccountPhonenumberAssignPost) | **POST** /v1/account/phonenumber/assign | Assign Number |
| [**v1AccountPhonenumberDisconnectPost**](PhoneNumberApi.md#v1AccountPhonenumberDisconnectPost) | **POST** /v1/account/phonenumber/disconnect | Disconnect Number |
| [**v1AccountPhonenumberGet**](PhoneNumberApi.md#v1AccountPhonenumberGet) | **GET** /v1/account/phonenumber | Get Unassigned Numbers List |
| [**v1AccountPhonenumberPost**](PhoneNumberApi.md#v1AccountPhonenumberPost) | **POST** /v1/account/phonenumber | Purchase Number |
| [**v1AccountPhonenumberUnassignPost**](PhoneNumberApi.md#v1AccountPhonenumberUnassignPost) | **POST** /v1/account/phonenumber/unassign | Unassign Number |
| [**v1PhonenumberSearchGet**](PhoneNumberApi.md#v1PhonenumberSearchGet) | **GET** /v1/phonenumber/search | Search New Numbers |


<a id="v1AccountAccountidPhonenumberGet"></a>
# **v1AccountAccountidPhonenumberGet**
> ServiceDocsAccountPhonenumberGetAll v1AccountAccountidPhonenumberGet(accountid, startKey, pageSize)

Get Assigned Numbers List

Access all phone numbers assigned to a CPaaS account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    String accountid = "accountid_example"; // String | Account ID, 32 alpha numeric
    String startKey = "startKey_example"; // String | Start key for pagination, obtained from previous responses
    Integer pageSize = 56; // Integer | Number of records to return per page (range: 1 to 50)
    try {
      ServiceDocsAccountPhonenumberGetAll result = apiInstance.v1AccountAccountidPhonenumberGet(accountid, startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountAccountidPhonenumberGet");
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
| **startKey** | **String**| Start key for pagination, obtained from previous responses | [optional] |
| **pageSize** | **Integer**| Number of records to return per page (range: 1 to 50) | [optional] |

### Return type

[**ServiceDocsAccountPhonenumberGetAll**](ServiceDocsAccountPhonenumberGetAll.md)

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

<a id="v1AccountPhonenumberAssignPost"></a>
# **v1AccountPhonenumberAssignPost**
> ServiceAPIResponseStatusCodeOnly v1AccountPhonenumberAssignPost(payload)

Assign Number

Assign a purchased phone number to an account.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    ServiceDocsPhonenumberAssignPayload payload = new ServiceDocsPhonenumberAssignPayload(); // ServiceDocsPhonenumberAssignPayload | assignment payload
    try {
      ServiceAPIResponseStatusCodeOnly result = apiInstance.v1AccountPhonenumberAssignPost(payload);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountPhonenumberAssignPost");
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
| **payload** | [**ServiceDocsPhonenumberAssignPayload**](ServiceDocsPhonenumberAssignPayload.md)| assignment payload | |

### Return type

[**ServiceAPIResponseStatusCodeOnly**](ServiceAPIResponseStatusCodeOnly.md)

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

<a id="v1AccountPhonenumberDisconnectPost"></a>
# **v1AccountPhonenumberDisconnectPost**
> ServiceAPIResponseStatusCodeOnly v1AccountPhonenumberDisconnectPost(payload)

Disconnect Number

Disconnecting a phone number from a CPaaS account relinquishes ownership of the number back to the carrier.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    ServiceDocsPhonenumberUnassignPayload payload = new ServiceDocsPhonenumberUnassignPayload(); // ServiceDocsPhonenumberUnassignPayload | disconnect payload
    try {
      ServiceAPIResponseStatusCodeOnly result = apiInstance.v1AccountPhonenumberDisconnectPost(payload);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountPhonenumberDisconnectPost");
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
| **payload** | [**ServiceDocsPhonenumberUnassignPayload**](ServiceDocsPhonenumberUnassignPayload.md)| disconnect payload | |

### Return type

[**ServiceAPIResponseStatusCodeOnly**](ServiceAPIResponseStatusCodeOnly.md)

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

<a id="v1AccountPhonenumberGet"></a>
# **v1AccountPhonenumberGet**
> ServiceDocsAccountPhonenumberGetAll v1AccountPhonenumberGet(startKey, pageSize)

Get Unassigned Numbers List

Obtain all phone numbers that have not been assigned to a CPaaS account within your organization.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    String startKey = "startKey_example"; // String | Start key for pagination, obtained from previous responses
    Integer pageSize = 56; // Integer | Number of records to return per page (range: 1 to 50)
    try {
      ServiceDocsAccountPhonenumberGetAll result = apiInstance.v1AccountPhonenumberGet(startKey, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountPhonenumberGet");
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
| **startKey** | **String**| Start key for pagination, obtained from previous responses | [optional] |
| **pageSize** | **Integer**| Number of records to return per page (range: 1 to 50) | [optional] |

### Return type

[**ServiceDocsAccountPhonenumberGetAll**](ServiceDocsAccountPhonenumberGetAll.md)

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

<a id="v1AccountPhonenumberPost"></a>
# **v1AccountPhonenumberPost**
> ServiceDocsOrderPhonenumber v1AccountPhonenumberPost(phonenumber)

Purchase Number

Purchase or activate a phone number for CPaaS accounts within your business.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    List<String> phonenumber = Arrays.asList(); // List<String> | phonenumber fields
    try {
      ServiceDocsOrderPhonenumber result = apiInstance.v1AccountPhonenumberPost(phonenumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountPhonenumberPost");
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
| **phonenumber** | [**List&lt;String&gt;**](String.md)| phonenumber fields | |

### Return type

[**ServiceDocsOrderPhonenumber**](ServiceDocsOrderPhonenumber.md)

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

<a id="v1AccountPhonenumberUnassignPost"></a>
# **v1AccountPhonenumberUnassignPost**
> ServiceAPIResponseStatusCodeOnly v1AccountPhonenumberUnassignPost(payload)

Unassign Number

Remove a phone number from an account and place it back on the list of unassigned phone numbers.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    ServiceDocsPhonenumberUnassignPayload payload = new ServiceDocsPhonenumberUnassignPayload(); // ServiceDocsPhonenumberUnassignPayload | unassign payload
    try {
      ServiceAPIResponseStatusCodeOnly result = apiInstance.v1AccountPhonenumberUnassignPost(payload);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1AccountPhonenumberUnassignPost");
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
| **payload** | [**ServiceDocsPhonenumberUnassignPayload**](ServiceDocsPhonenumberUnassignPayload.md)| unassign payload | |

### Return type

[**ServiceAPIResponseStatusCodeOnly**](ServiceAPIResponseStatusCodeOnly.md)

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

<a id="v1PhonenumberSearchGet"></a>
# **v1PhonenumberSearchGet**
> ServiceDocsPhonenumberSearchGetAll v1PhonenumberSearchGet(areaCode, quantity)

Search New Numbers

Conduct a search for available phone numbers for purchase within an area code.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.PhoneNumberApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    PhoneNumberApi apiInstance = new PhoneNumberApi(defaultClient);
    String areaCode = "areaCode_example"; // String | Area code (exactly 3 numeric characters) example: 610 or 484
    Integer quantity = 100; // Integer | Number of records to return (range: 1 to 100, defaults to 100 if not provided)
    try {
      ServiceDocsPhonenumberSearchGetAll result = apiInstance.v1PhonenumberSearchGet(areaCode, quantity);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PhoneNumberApi#v1PhonenumberSearchGet");
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
| **areaCode** | **String**| Area code (exactly 3 numeric characters) example: 610 or 484 | |
| **quantity** | **Integer**| Number of records to return (range: 1 to 100, defaults to 100 if not provided) | [optional] [default to 100] |

### Return type

[**ServiceDocsPhonenumberSearchGetAll**](ServiceDocsPhonenumberSearchGetAll.md)

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

