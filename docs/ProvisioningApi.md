# ProvisioningApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1ApBrandBrandFamilyFamilyGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyGet) | **GET** /v1/ap/brand/{brand}/family/{family} | Get Family
[**v1ApBrandBrandFamilyFamilyModelGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model | Get Model List
[**v1ApBrandBrandFamilyFamilyModelModelGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model} | Get Model
[**v1ApBrandBrandFamilyFamilyModelModelTemplateGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template | Get Template List
[**v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template/{template} | Get Template
[**v1ApBrandBrandFamilyGet**](ProvisioningApi.md#v1ApBrandBrandFamilyGet) | **GET** /v1/ap/brand/{brand}/family | Get Family List
[**v1ApBrandBrandGet**](ProvisioningApi.md#v1ApBrandBrandGet) | **GET** /v1/ap/brand/{brand} | Get Brand
[**v1ApBrandGet**](ProvisioningApi.md#v1ApBrandGet) | **GET** /v1/ap/brand | Get Brand
[**v1ApConfigfileGeneratePost**](ProvisioningApi.md#v1ApConfigfileGeneratePost) | **POST** /v1/ap/configfile/generate | Generate config file



## v1ApBrandBrandFamilyFamilyGet

Get Family

Retrieve a family's details by the randomly generated ID.

### Example

```bash
 v1ApBrandBrandFamilyFamilyGet brand=value family=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **family** | **String** | family |

### Return type

[**ProvisioningDocsDocsFamilyOutputSingle**](ProvisioningDocsDocsFamilyOutputSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandFamilyFamilyModelGet

Get Model List

Retrieve a list of all models within a family for a brand (e.g., Yealink and Polycom).

### Example

```bash
 v1ApBrandBrandFamilyFamilyModelGet brand=value family=value  model_name=value  page_size=value  start_key=value  status=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **family** | **String** | family |
 **modelName** | **String** |  | [optional]
 **pageSize** | **Integer** |  | [optional]
 **startKey** | **String** |  | [optional]
 **status** | **String** |  | [optional]

### Return type

[**ProvisioningDocsDocsModelOutput**](ProvisioningDocsDocsModelOutput.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandFamilyFamilyModelModelGet

Get Model

Retrieve a model's details by the randomly generated ID.

### Example

```bash
 v1ApBrandBrandFamilyFamilyModelModelGet brand=value family=value model=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **family** | **String** | family |
 **model** | **String** | model |

### Return type

[**ProvisioningDocsDocsModelOutputSingle**](ProvisioningDocsDocsModelOutputSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandFamilyFamilyModelModelTemplateGet

Get Template List

Retrieve a list of all templates for a model within a brand (e.g., Yealink and Polycom).

### Example

```bash
 v1ApBrandBrandFamilyFamilyModelModelTemplateGet brand=value family=value model=value  firmware=value  page_size=value  start_key=value  status=value  template_name=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **family** | **String** | family |
 **model** | **String** | model |
 **firmware** | **String** |  | [optional]
 **pageSize** | **Integer** |  | [optional]
 **startKey** | **String** |  | [optional]
 **status** | **String** |  | [optional]
 **templateName** | **String** |  | [optional]

### Return type

[**ProvisioningDocsDocsTemplatesOutput**](ProvisioningDocsDocsTemplatesOutput.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet

Get Template

Retrieve details about a template for a model by the randomly generated ID.

### Example

```bash
 v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet brand=value family=value model=value template=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **family** | **String** | family |
 **model** | **String** | model |
 **template** | **String** | template |

### Return type

[**ProvisioningDocsDocsTemplateOutputSingle**](ProvisioningDocsDocsTemplateOutputSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandFamilyGet

Get Family List

Retrieve a list of all families for a brand (e.g., Yealink and Polycom).

### Example

```bash
 v1ApBrandBrandFamilyGet brand=value  family_name=value  page_size=value  start_key=value  status=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand |
 **familyName** | **String** |  | [optional]
 **pageSize** | **Integer** |  | [optional]
 **startKey** | **String** |  | [optional]
 **status** | **String** |  | [optional]

### Return type

[**ProvisioningDocsDocsFamilyOutput**](ProvisioningDocsDocsFamilyOutput.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandBrandGet

Get Brand

Retrieve a brand's details by the randomly generated ID.

### Example

```bash
 v1ApBrandBrandGet brand=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brand** | **String** | brand id to retrieve a brand |

### Return type

[**ProvisioningDocsDocsBrandOutputSingle**](ProvisioningDocsDocsBrandOutputSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApBrandGet

Get Brand

Retrieve a list of all brands (e.g., Yealink and Polycom) by client.

### Example

```bash
 v1ApBrandGet  brand_name=value  page_size=value  start_key=value  status=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **brandName** | **String** |  | [optional]
 **pageSize** | **Integer** |  | [optional]
 **startKey** | **String** |  | [optional]
 **status** | **String** |  | [optional]

### Return type

[**ProvisioningDocsDocsBrandsOutput**](ProvisioningDocsDocsBrandsOutput.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1ApConfigfileGeneratePost

Generate config file

Generate a configuration file that includes a list of parameters passed to the specified template_id in the request payload, with populated values returned in the response.

### Example

```bash
 v1ApConfigfileGeneratePost
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **params** | [**ModelsGenerateConfigFileRequest**](ModelsGenerateConfigFileRequest.md) | body params to generate config file |

### Return type

[**ProvisioningDocsDocsConfigFileOutput**](ProvisioningDocsDocsConfigFileOutput.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

