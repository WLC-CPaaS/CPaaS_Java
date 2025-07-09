# ProvisioningApi

All URIs are relative to *http://api.beta.cpaaslabs.net*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v1AccountAccountIDProvisionFilenameGet**](ProvisioningApi.md#v1AccountAccountIDProvisionFilenameGet) | **GET** /v1/account/{accountID}/provision/{filename} | Get Config File Details |
| [**v1ApBrandBrandFamilyFamilyGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyGet) | **GET** /v1/ap/brand/{brand}/family/{family} | Get Family Details |
| [**v1ApBrandBrandFamilyFamilyModelGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model | Get Model List |
| [**v1ApBrandBrandFamilyFamilyModelModelGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model} | Get Model Details |
| [**v1ApBrandBrandFamilyFamilyModelModelTemplateGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template | Get Template List |
| [**v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template/{template} | Get Template Details |
| [**v1ApBrandBrandFamilyGet**](ProvisioningApi.md#v1ApBrandBrandFamilyGet) | **GET** /v1/ap/brand/{brand}/family | Get Family List |
| [**v1ApBrandBrandGet**](ProvisioningApi.md#v1ApBrandBrandGet) | **GET** /v1/ap/brand/{brand} | Get Brand Details |
| [**v1ApBrandGet**](ProvisioningApi.md#v1ApBrandGet) | **GET** /v1/ap/brand | Get Brand List |
| [**v1ApConfigfileGeneratePost**](ProvisioningApi.md#v1ApConfigfileGeneratePost) | **POST** /v1/ap/configfile/generate | Generate Config File |


<a id="v1AccountAccountIDProvisionFilenameGet"></a>
# **v1AccountAccountIDProvisionFilenameGet**
> File v1AccountAccountIDProvisionFilenameGet(accountID, filename)

Get Config File Details

Retrieve the configuration details (e.g., settings and parameters) for a device.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String accountID = "accountID_example"; // String | Account ID, 32 alpha numeric
    String filename = "filename_example"; // String | Name of config file
    try {
      File result = apiInstance.v1AccountAccountIDProvisionFilenameGet(accountID, filename);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1AccountAccountIDProvisionFilenameGet");
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
| **filename** | **String**| Name of config file | |

### Return type

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |

<a id="v1ApBrandBrandFamilyFamilyGet"></a>
# **v1ApBrandBrandFamilyFamilyGet**
> ProvisioningDocsDocsFamilyOutputSingle v1ApBrandBrandFamilyFamilyGet(brand, family)

Get Family Details

Retrieve a family&#39;s details by the randomly generated ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String family = "family_example"; // String | family
    try {
      ProvisioningDocsDocsFamilyOutputSingle result = apiInstance.v1ApBrandBrandFamilyFamilyGet(brand, family);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyFamilyGet");
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
| **brand** | **String**| brand | |
| **family** | **String**| family | |

### Return type

[**ProvisioningDocsDocsFamilyOutputSingle**](ProvisioningDocsDocsFamilyOutputSingle.md)

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

<a id="v1ApBrandBrandFamilyFamilyModelGet"></a>
# **v1ApBrandBrandFamilyFamilyModelGet**
> ProvisioningDocsDocsModelOutput v1ApBrandBrandFamilyFamilyModelGet(brand, family, modelName, pageSize, startKey, status)

Get Model List

Retrieve a list of all models within a family for a brand (e.g., Yealink and Polycom).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String family = "family_example"; // String | family
    String modelName = "modelName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    String status = "active"; // String | 
    try {
      ProvisioningDocsDocsModelOutput result = apiInstance.v1ApBrandBrandFamilyFamilyModelGet(brand, family, modelName, pageSize, startKey, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyFamilyModelGet");
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
| **brand** | **String**| brand | |
| **family** | **String**| family | |
| **modelName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **status** | **String**|  | [optional] [enum: active, inactive] |

### Return type

[**ProvisioningDocsDocsModelOutput**](ProvisioningDocsDocsModelOutput.md)

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

<a id="v1ApBrandBrandFamilyFamilyModelModelGet"></a>
# **v1ApBrandBrandFamilyFamilyModelModelGet**
> ProvisioningDocsDocsModelOutputSingle v1ApBrandBrandFamilyFamilyModelModelGet(brand, family, model)

Get Model Details

Retrieve a model&#39;s details by the randomly generated ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String family = "family_example"; // String | family
    String model = "model_example"; // String | model
    try {
      ProvisioningDocsDocsModelOutputSingle result = apiInstance.v1ApBrandBrandFamilyFamilyModelModelGet(brand, family, model);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyFamilyModelModelGet");
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
| **brand** | **String**| brand | |
| **family** | **String**| family | |
| **model** | **String**| model | |

### Return type

[**ProvisioningDocsDocsModelOutputSingle**](ProvisioningDocsDocsModelOutputSingle.md)

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

<a id="v1ApBrandBrandFamilyFamilyModelModelTemplateGet"></a>
# **v1ApBrandBrandFamilyFamilyModelModelTemplateGet**
> ProvisioningDocsDocsTemplatesOutput v1ApBrandBrandFamilyFamilyModelModelTemplateGet(brand, family, model, firmware, pageSize, startKey, status, templateName)

Get Template List

Retrieve a list of all templates for a model within a brand (e.g., Yealink and Polycom).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String family = "family_example"; // String | family
    String model = "model_example"; // String | model
    String firmware = "firmware_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    String status = "active"; // String | 
    String templateName = "templateName_example"; // String | 
    try {
      ProvisioningDocsDocsTemplatesOutput result = apiInstance.v1ApBrandBrandFamilyFamilyModelModelTemplateGet(brand, family, model, firmware, pageSize, startKey, status, templateName);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyFamilyModelModelTemplateGet");
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
| **brand** | **String**| brand | |
| **family** | **String**| family | |
| **model** | **String**| model | |
| **firmware** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **status** | **String**|  | [optional] [enum: active, inactive] |
| **templateName** | **String**|  | [optional] |

### Return type

[**ProvisioningDocsDocsTemplatesOutput**](ProvisioningDocsDocsTemplatesOutput.md)

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

<a id="v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet"></a>
# **v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet**
> ProvisioningDocsDocsTemplateOutputSingle v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet(brand, family, model, template)

Get Template Details

Retrieve details about a template for a model by the randomly generated ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String family = "family_example"; // String | family
    String model = "model_example"; // String | model
    String template = "template_example"; // String | template
    try {
      ProvisioningDocsDocsTemplateOutputSingle result = apiInstance.v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet(brand, family, model, template);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet");
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
| **brand** | **String**| brand | |
| **family** | **String**| family | |
| **model** | **String**| model | |
| **template** | **String**| template | |

### Return type

[**ProvisioningDocsDocsTemplateOutputSingle**](ProvisioningDocsDocsTemplateOutputSingle.md)

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

<a id="v1ApBrandBrandFamilyGet"></a>
# **v1ApBrandBrandFamilyGet**
> ProvisioningDocsDocsFamilyOutput v1ApBrandBrandFamilyGet(brand, familyName, pageSize, startKey, status)

Get Family List

Retrieve a list of all families for a brand (e.g., Yealink and Polycom).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand
    String familyName = "familyName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    String status = "active"; // String | 
    try {
      ProvisioningDocsDocsFamilyOutput result = apiInstance.v1ApBrandBrandFamilyGet(brand, familyName, pageSize, startKey, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandFamilyGet");
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
| **brand** | **String**| brand | |
| **familyName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **status** | **String**|  | [optional] [enum: active, inactive] |

### Return type

[**ProvisioningDocsDocsFamilyOutput**](ProvisioningDocsDocsFamilyOutput.md)

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

<a id="v1ApBrandBrandGet"></a>
# **v1ApBrandBrandGet**
> ProvisioningDocsDocsBrandOutputSingle v1ApBrandBrandGet(brand)

Get Brand Details

Retrieve a brand&#39;s details by the randomly generated ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brand = "brand_example"; // String | brand id to retrieve a brand
    try {
      ProvisioningDocsDocsBrandOutputSingle result = apiInstance.v1ApBrandBrandGet(brand);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandBrandGet");
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
| **brand** | **String**| brand id to retrieve a brand | |

### Return type

[**ProvisioningDocsDocsBrandOutputSingle**](ProvisioningDocsDocsBrandOutputSingle.md)

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

<a id="v1ApBrandGet"></a>
# **v1ApBrandGet**
> ProvisioningDocsDocsBrandsOutput v1ApBrandGet(brandName, pageSize, startKey, status)

Get Brand List

Retrieve a list of all brands (e.g., Yealink and Polycom) by client.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    String brandName = "brandName_example"; // String | 
    Integer pageSize = 56; // Integer | 
    String startKey = "startKey_example"; // String | 
    String status = "active"; // String | 
    try {
      ProvisioningDocsDocsBrandsOutput result = apiInstance.v1ApBrandGet(brandName, pageSize, startKey, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApBrandGet");
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
| **brandName** | **String**|  | [optional] |
| **pageSize** | **Integer**|  | [optional] |
| **startKey** | **String**|  | [optional] |
| **status** | **String**|  | [optional] [enum: active, inactive] |

### Return type

[**ProvisioningDocsDocsBrandsOutput**](ProvisioningDocsDocsBrandsOutput.md)

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

<a id="v1ApConfigfileGeneratePost"></a>
# **v1ApConfigfileGeneratePost**
> ProvisioningDocsDocsConfigFileOutput v1ApConfigfileGeneratePost(params)

Generate Config File

Generate a configuration file that includes a list of parameters passed to the specified template_id in the request payload, with populated values returned in the response.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProvisioningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://api.beta.cpaaslabs.net");
    
    // Configure API key authorization: BearerAuth
    ApiKeyAuth BearerAuth = (ApiKeyAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //BearerAuth.setApiKeyPrefix("Token");

    ProvisioningApi apiInstance = new ProvisioningApi(defaultClient);
    ModelsGenerateConfigFileRequest params = new ModelsGenerateConfigFileRequest(); // ModelsGenerateConfigFileRequest | body params to generate config file
    try {
      ProvisioningDocsDocsConfigFileOutput result = apiInstance.v1ApConfigfileGeneratePost(params);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProvisioningApi#v1ApConfigfileGeneratePost");
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
| **params** | [**ModelsGenerateConfigFileRequest**](ModelsGenerateConfigFileRequest.md)| body params to generate config file | |

### Return type

[**ProvisioningDocsDocsConfigFileOutput**](ProvisioningDocsDocsConfigFileOutput.md)

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
| **500** | Internal Server Error |  -  |

