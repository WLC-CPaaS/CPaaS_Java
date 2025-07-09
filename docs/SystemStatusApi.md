# SystemStatusApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1ApPingGet**](SystemStatusApi.md#v1ApPingGet) | **GET** /v1/ap/ping | Provisioning Ping |
| [**v1PingGet**](SystemStatusApi.md#v1PingGet) | **GET** /v1/ping | Ping Backend |
| [**v1PingseccognitoGet**](SystemStatusApi.md#v1PingseccognitoGet) | **GET** /v1/pingseccognito | Ping Cognito |
| [**v1SystemStatusGet**](SystemStatusApi.md#v1SystemStatusGet) | **GET** /v1/system_status | Get System Status |


<a id="v1ApPingGet"></a>
# **v1ApPingGet**
> ProvisioningDocsDocsPingOutput v1ApPingGet()

Provisioning Ping

Ping the provisioning service.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SystemStatusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    SystemStatusApi apiInstance = new SystemStatusApi(defaultClient);
    try {
      ProvisioningDocsDocsPingOutput result = apiInstance.v1ApPingGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemStatusApi#v1ApPingGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ProvisioningDocsDocsPingOutput**](ProvisioningDocsDocsPingOutput.md)

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
| **500** | Internal Server Error |  -  |

<a id="v1PingGet"></a>
# **v1PingGet**
> ServiceDocsPingGet v1PingGet()

Ping Backend

Get the ping message.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SystemStatusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    SystemStatusApi apiInstance = new SystemStatusApi(defaultClient);
    try {
      ServiceDocsPingGet result = apiInstance.v1PingGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemStatusApi#v1PingGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ServiceDocsPingGet**](ServiceDocsPingGet.md)

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

<a id="v1PingseccognitoGet"></a>
# **v1PingseccognitoGet**
> ServiceDocsPingGet v1PingseccognitoGet()

Ping Cognito

Get a secure ping message.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SystemStatusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    SystemStatusApi apiInstance = new SystemStatusApi(defaultClient);
    try {
      ServiceDocsPingGet result = apiInstance.v1PingseccognitoGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemStatusApi#v1PingseccognitoGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ServiceDocsPingGet**](ServiceDocsPingGet.md)

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

<a id="v1SystemStatusGet"></a>
# **v1SystemStatusGet**
> ServiceDocsSystemStatusGetSingle v1SystemStatusGet()

Get System Status

Get the system status.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SystemStatusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    SystemStatusApi apiInstance = new SystemStatusApi(defaultClient);
    try {
      ServiceDocsSystemStatusGetSingle result = apiInstance.v1SystemStatusGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemStatusApi#v1SystemStatusGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ServiceDocsSystemStatusGetSingle**](ServiceDocsSystemStatusGetSingle.md)

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

