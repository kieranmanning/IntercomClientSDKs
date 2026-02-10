# DeviceTokenRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grant_type** | [**GrantTypeEnum**](GrantTypeEnum.md) |  | 
**device_code** | **str** |  | 
**client_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.device_token_request import DeviceTokenRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceTokenRequest from a JSON string
device_token_request_instance = DeviceTokenRequest.from_json(json)
# print the JSON string representation of the object
print(DeviceTokenRequest.to_json())

# convert the object into a dict
device_token_request_dict = device_token_request_instance.to_dict()
# create an instance of DeviceTokenRequest from a dict
device_token_request_from_dict = DeviceTokenRequest.from_dict(device_token_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


