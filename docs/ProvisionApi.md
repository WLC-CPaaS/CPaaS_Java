# ProvisionApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AccountAccountIDProvisionFilenameGet**](ProvisionApi.md#v1AccountAccountIDProvisionFilenameGet) | **GET** /v1/account/{accountID}/provision/{filename} | 



## v1AccountAccountIDProvisionFilenameGet



Retrieve the configuration details (e.g., settings and parameters) for a device.

### Example

```bash
 v1AccountAccountIDProvisionFilenameGet accountID=value filename=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountID** | **String** | Account ID, 32 alpha numeric |
 **filename** | **String** | Name of config file |

### Return type

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

