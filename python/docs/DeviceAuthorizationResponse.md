# DeviceAuthorizationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**device_code** | **str** |  | 
**user_code** | **str** |  | 
**verification_uri** | **str** |  | 
**expires_in** | **int** |  | 
**interval** | **int** |  | 

## Example

```python
from openapi_client.models.device_authorization_response import DeviceAuthorizationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceAuthorizationResponse from a JSON string
device_authorization_response_instance = DeviceAuthorizationResponse.from_json(json)
# print the JSON string representation of the object
print(DeviceAuthorizationResponse.to_json())

# convert the object into a dict
device_authorization_response_dict = device_authorization_response_instance.to_dict()
# create an instance of DeviceAuthorizationResponse from a dict
device_authorization_response_from_dict = DeviceAuthorizationResponse.from_dict(device_authorization_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


