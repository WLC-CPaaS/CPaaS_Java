

# TypesResourceRecord


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**value** | **String** | The current or new DNS record value, not to exceed 4,000 characters. In the case of a DELETE action, if the current value does not match the actual value, an error is returned. For descriptions about how to format Value for different record types, see [Supported DNS Resource Record Types]in the Amazon Route 53 Developer Guide.  You can specify more than one value for all record types except CNAME and SOA .  If you&#39;re creating an alias resource record set, omit Value .  [Supported DNS Resource Record Types]: https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html  This member is required. |  [optional] |



