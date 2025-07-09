

# ServiceVOIPDeviceAddEdit2


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**callForward** | [**ModelsCallForward**](ModelsCallForward.md) |  |  [optional] |
|**callerId** | [**ServiceVOIPDeviceAddEdit3c**](ServiceVOIPDeviceAddEdit3c.md) |  |  [optional] |
|**deviceType** | [**DeviceTypeEnum**](#DeviceTypeEnum) |  |  [optional] |
|**doNotDisturb** | [**ModelsVOIPSharedDoNotDisturb**](ModelsVOIPSharedDoNotDisturb.md) |  |  [optional] |
|**enabled** | **Boolean** | cannot use required, else it has to be true and false is not allowed |  [optional] |
|**macAddress** | **String** | dont use mac, it enforces :, which voip does not like |  [optional] |
|**media** | [**ServiceVOIPDeviceAddEdit3d**](ServiceVOIPDeviceAddEdit3d.md) |  |  [optional] |
|**musicOnHold** | [**ModelsMusicOnHold**](ModelsMusicOnHold.md) |  |  [optional] |
|**name** | **String** |  |  |
|**ownerId** | **String** | json omitempty is needed else voip fails on \&quot;\&quot; for owner_id |  [optional] |
|**provision** | [**ServiceVOIPDeviceAddEditProvision**](ServiceVOIPDeviceAddEditProvision.md) |  |  [optional] |
|**sip** | [**ServiceVOIPDeviceAddEdit3a**](ServiceVOIPDeviceAddEdit3a.md) |  |  |



## Enum: DeviceTypeEnum

| Name | Value |
|---- | -----|
| SOFTPHONE | &quot;softphone&quot; |
| SIP_URI | &quot;sip_uri&quot; |
| SIP_DEVICE | &quot;sip_device&quot; |



