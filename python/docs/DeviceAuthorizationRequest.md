# DeviceAuthorizationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** |  | 
**scope** | **str** |  | [optional] 
**device_type** | **str** |  | 
**device_os** | **str** |  | 

## Example

```python
from openapi_client.models.device_authorization_request import DeviceAuthorizationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceAuthorizationRequest from a JSON string
device_authorization_request_instance = DeviceAuthorizationRequest.from_json(json)
# print the JSON string representation of the object
print(DeviceAuthorizationRequest.to_json())

# convert the object into a dict
device_authorization_request_dict = device_authorization_request_instance.to_dict()
# create an instance of DeviceAuthorizationRequest from a dict
device_authorization_request_from_dict = DeviceAuthorizationRequest.from_dict(device_authorization_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


