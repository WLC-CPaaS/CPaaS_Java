# E911Api

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1E911Get**](E911Api.md#v1E911Get) | **GET** /v1/e911 | Get E911 List |
| [**v1E911LocationLocationIDActivatePut**](E911Api.md#v1E911LocationLocationIDActivatePut) | **PUT** /v1/e911/location/{locationID}/activate | Activate E911 Location |
| [**v1E911LocationLocationIDDelete**](E911Api.md#v1E911LocationLocationIDDelete) | **DELETE** /v1/e911/location/{locationID} | Delete E911 Location |
| [**v1E911LocationValidatePut**](E911Api.md#v1E911LocationValidatePut) | **PUT** /v1/e911/location/validate | Validate a Location |
| [**v1E911PhoneNumberDelete**](E911Api.md#v1E911PhoneNumberDelete) | **DELETE** /v1/e911/{phoneNumber} | Delete E911 Phone Number |
| [**v1E911PhoneNumberLocationActiveGet**](E911Api.md#v1E911PhoneNumberLocationActiveGet) | **GET** /v1/e911/{phoneNumber}/location/active | Get Actvie Location for a Phone Number |
| [**v1E911PhoneNumberLocationGet**](E911Api.md#v1E911PhoneNumberLocationGet) | **GET** /v1/e911/{phoneNumber}/location | Get Location List for Phone Number |
| [**v1E911Post**](E911Api.md#v1E911Post) | **POST** /v1/e911 | Create an E911 Location |


<a id="v1E911Get"></a>
# **v1E911Get**
> ServiceDocsE911URIsApiOutput v1E911Get()

Get E911 List

Obtain e911 URIs associated with the provided account ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    try {
      ServiceDocsE911URIsApiOutput result = apiInstance.v1E911Get();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911Get");
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

[**ServiceDocsE911URIsApiOutput**](ServiceDocsE911URIsApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with e911 URIs |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911LocationLocationIDActivatePut"></a>
# **v1E911LocationLocationIDActivatePut**
> ServiceDocsE911ActiveLocationOutput v1E911LocationLocationIDActivatePut(locationID)

Activate E911 Location

Edit the provision location.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    String locationID = "locationID_example"; // String | Location ID
    try {
      ServiceDocsE911ActiveLocationOutput result = apiInstance.v1E911LocationLocationIDActivatePut(locationID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911LocationLocationIDActivatePut");
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
| **locationID** | **String**| Location ID | |

### Return type

[**ServiceDocsE911ActiveLocationOutput**](ServiceDocsE911ActiveLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with location activate status |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911LocationLocationIDDelete"></a>
# **v1E911LocationLocationIDDelete**
> ServiceDocsE911RemoveLocationOutput v1E911LocationLocationIDDelete(locationID)

Delete E911 Location

Remove the location.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    String locationID = "locationID_example"; // String | Location ID
    try {
      ServiceDocsE911RemoveLocationOutput result = apiInstance.v1E911LocationLocationIDDelete(locationID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911LocationLocationIDDelete");
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
| **locationID** | **String**| Location ID | |

### Return type

[**ServiceDocsE911RemoveLocationOutput**](ServiceDocsE911RemoveLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with location remove status |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911LocationValidatePut"></a>
# **v1E911LocationValidatePut**
> ServiceDocsE911ValidateLocationOutput v1E911LocationValidatePut(reqBody)

Validate a Location

Validate the location details.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    ServiceE911ValidateLocationInput reqBody = new ServiceE911ValidateLocationInput(); // ServiceE911ValidateLocationInput | location details
    try {
      ServiceDocsE911ValidateLocationOutput result = apiInstance.v1E911LocationValidatePut(reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911LocationValidatePut");
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
| **reqBody** | [**ServiceE911ValidateLocationInput**](ServiceE911ValidateLocationInput.md)| location details | |

### Return type

[**ServiceDocsE911ValidateLocationOutput**](ServiceDocsE911ValidateLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with location details |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911PhoneNumberDelete"></a>
# **v1E911PhoneNumberDelete**
> ServiceDocsE911RemoveURIApiOutput v1E911PhoneNumberDelete(phoneNumber)

Delete E911 Phone Number

Delete the e911 URI connected with the account URI.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    String phoneNumber = "phoneNumber_example"; // String | Phone Number
    try {
      ServiceDocsE911RemoveURIApiOutput result = apiInstance.v1E911PhoneNumberDelete(phoneNumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911PhoneNumberDelete");
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
| **phoneNumber** | **String**| Phone Number | |

### Return type

[**ServiceDocsE911RemoveURIApiOutput**](ServiceDocsE911RemoveURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911PhoneNumberLocationActiveGet"></a>
# **v1E911PhoneNumberLocationActiveGet**
> ServiceDocsE911ActiveLocationURIApiOutput v1E911PhoneNumberLocationActiveGet(phoneNumber)

Get Actvie Location for a Phone Number

Get the e911 location connected with the URI.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    String phoneNumber = "phoneNumber_example"; // String | Phone Number
    try {
      ServiceDocsE911ActiveLocationURIApiOutput result = apiInstance.v1E911PhoneNumberLocationActiveGet(phoneNumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911PhoneNumberLocationActiveGet");
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
| **phoneNumber** | **String**| Phone Number | |

### Return type

[**ServiceDocsE911ActiveLocationURIApiOutput**](ServiceDocsE911ActiveLocationURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with e911 Active Location URI |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911PhoneNumberLocationGet"></a>
# **v1E911PhoneNumberLocationGet**
> ServiceDocsE911LocationsURIApiOutput v1E911PhoneNumberLocationGet(phoneNumber)

Get Location List for Phone Number

Access a list of the e911 locations associated with the provided URI.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    String phoneNumber = "phoneNumber_example"; // String | Phone Number
    try {
      ServiceDocsE911LocationsURIApiOutput result = apiInstance.v1E911PhoneNumberLocationGet(phoneNumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911PhoneNumberLocationGet");
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
| **phoneNumber** | **String**| Phone Number | |

### Return type

[**ServiceDocsE911LocationsURIApiOutput**](ServiceDocsE911LocationsURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with e911 Locations URI |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

<a id="v1E911Post"></a>
# **v1E911Post**
> ServiceDocsE911AddLocationOutput v1E911Post(reqBody)

Create an E911 Location

Enter new location details.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.E911Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    E911Api apiInstance = new E911Api(defaultClient);
    ServiceE911AddLocationInput reqBody = new ServiceE911AddLocationInput(); // ServiceE911AddLocationInput | location details
    try {
      ServiceDocsE911AddLocationOutput result = apiInstance.v1E911Post(reqBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling E911Api#v1E911Post");
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
| **reqBody** | [**ServiceE911AddLocationInput**](ServiceE911AddLocationInput.md)| location details | |

### Return type

[**ServiceDocsE911AddLocationOutput**](ServiceDocsE911AddLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with location details |  -  |
| **403** | Authorization failed or root account not allowed |  -  |
| **500** | Internal server error, including environment credential issues, HTTP request failures, or XML unmarshaling errors |  -  |

