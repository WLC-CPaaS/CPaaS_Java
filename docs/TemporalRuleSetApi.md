# TemporalRuleSetApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AccountAccountIDTemporalrulesetGet**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetGet) | **GET** /v1/account/{accountID}/temporalruleset | Get Temporal Rule Set List
[**v1AccountAccountIDTemporalrulesetPost**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetPost) | **POST** /v1/account/{accountID}/temporalruleset | Create Temporal Rule Set
[**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete) | **DELETE** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Delete Temporal Rule Set
[**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet) | **GET** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Get Temporal Rule Set Details
[**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut) | **PUT** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Update Temporal Rule Set



## v1AccountAccountIDTemporalrulesetGet

Get Temporal Rule Set List

Access the temporal rule set list in an account.

### Example

```bash
 v1AccountAccountIDTemporalrulesetGet accountID=value  start_key=value  page_size=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alpha numeric |
 **startKey** | **String** | start_key for pagination that was returned as next_start_key from your previous call | [optional]
 **pageSize** | **Integer** | number of records to return, range 1 to 50 | [optional]

### Return type

[**ServiceDocsTemporalRuleSetGetAll**](ServiceDocsTemporalRuleSetGetAll.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountIDTemporalrulesetPost

Create Temporal Rule Set

Develop a new temporal rule set for an account.

### Example

```bash
 v1AccountAccountIDTemporalrulesetPost accountID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alphanumeric |
 **temporalruleset** | [**ServiceVOIPTemporalRuleSetAddEditData**](ServiceVOIPTemporalRuleSetAddEditData.md) | payload fields |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete

Delete Temporal Rule Set

Delete the temporal rule set from an account.

### Example

```bash
 v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete accountID=value temporalRuleSetID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alpha numeric |
 **temporalRuleSetID** | **String** | temporal rule set ID, 32 alpha numeric |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet

Get Temporal Rule Set Details

Acquire details about a temporal rule set in an account.

### Example

```bash
 v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet accountID=value temporalRuleSetID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alpha numeric |
 **temporalRuleSetID** | **String** | Temporal Ruleset ID, 32 alpha numeric |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut

Update Temporal Rule Set

Efficiently adjust the temporal rule set in an account.

### Example

```bash
 v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut accountID=value temporalRuleSetID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alpha numeric |
 **temporalRuleSetID** | **String** | Temporal Ruleset ID, 32 alpha numeric |
 **reqBody** | [**ServiceVOIPTemporalRuleSetAddEditData**](ServiceVOIPTemporalRuleSetAddEditData.md) | payload fields |

### Return type

[**ServiceDocsTemporalRuleSetGetSingle**](ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

