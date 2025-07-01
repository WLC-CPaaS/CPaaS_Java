# VoIpUserApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AccountAccountidUserGet**](VoIpUserApi.md#v1AccountAccountidUserGet) | **GET** /v1/account/{accountid}/user | Get User List
[**v1AccountAccountidUserPost**](VoIpUserApi.md#v1AccountAccountidUserPost) | **POST** /v1/account/{accountid}/user | Create User
[**v1AccountAccountidUserUseridDelete**](VoIpUserApi.md#v1AccountAccountidUserUseridDelete) | **DELETE** /v1/account/{accountid}/user/{userid} | Delete User
[**v1AccountAccountidUserUseridGet**](VoIpUserApi.md#v1AccountAccountidUserUseridGet) | **GET** /v1/account/{accountid}/user/{userid} | Get User Details
[**v1AccountAccountidUserUseridPut**](VoIpUserApi.md#v1AccountAccountidUserUseridPut) | **PUT** /v1/account/{accountid}/user/{userid} | Update User
[**v1AccountAccountidUserUseridUserauthPost**](VoIpUserApi.md#v1AccountAccountidUserUseridUserauthPost) | **POST** /v1/account/{accountid}/user/{userid}/userauth | Impersonate a User



## v1AccountAccountidUserGet

Get User List

Get a list of all VoIP users that includes first and last names, email addresses, extensions, and account statuses.

### Example

```bash
 v1AccountAccountidUserGet accountid=value  start_key=value  page_size=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **startKey** | **String** | start_key for pagination that was returned as next_start_key from your previous call | [optional]
 **pageSize** | **Integer** | number of records to return, range 1 to 50 | [optional]

### Return type

[**ServiceDocsUserGetAll**](ServiceDocsUserGetAll.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountidUserPost

Create User

Add new users to the account. When a user is added, the system generates their unique 32 alpha numeric ID.

### Example

```bash
 v1AccountAccountidUserPost accountid=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **user** | [**ServiceVOIPUserAdd2**](ServiceVOIPUserAdd2.md) | user fields |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountidUserUseridDelete

Delete User

Delete VoIP user access to maintain the security of your accounts.

### Example

```bash
 v1AccountAccountidUserUseridDelete accountid=value userid=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **userid** | **String** | User ID, 32 alpha numeric |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountidUserUseridGet

Get User Details

View specific user details.

### Example

```bash
 v1AccountAccountidUserUseridGet accountid=value userid=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **userid** | **String** | User ID, 32 alpha numeric |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountidUserUseridPut

Update User

Keep user information current. Modify the first and last name, extension, and other pertinent information.

### Example

```bash
 v1AccountAccountidUserUseridPut accountid=value userid=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **userid** | **String** | User ID, 32 alpha numeric |
 **user** | [**ServiceVOIPUserAdd2**](ServiceVOIPUserAdd2.md) | user fields |

### Return type

[**ServiceDocsUserGetSingle**](ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## v1AccountAccountidUserUseridUserauthPost

Impersonate a User

Impersonate as another user if you have access to admin.

### Example

```bash
 v1AccountAccountidUserUseridUserauthPost accountid=value userid=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountid** | **String** | Account ID, 32 alpha numeric |
 **userid** | **String** | User ID, 32 alpha numeric |
 **user** | [**ServiceVOIPImpersonateUser**](ServiceVOIPImpersonateUser.md) | Payload for impersonate a user |

### Return type

[**ServiceDocsImpersonateUserGetSingle**](ServiceDocsImpersonateUserGetSingle.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

