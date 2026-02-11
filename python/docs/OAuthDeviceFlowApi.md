# transparenc_sdk.OAuthDeviceFlowApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_oauth_device_authorization_create**](OAuthDeviceFlowApi.md#v1_oauth_device_authorization_create) | **POST** /api/v1/oauth/device-authorization/ | Start device authorization (Device Code Flow)
[**v1_oauth_token_create**](OAuthDeviceFlowApi.md#v1_oauth_token_create) | **POST** /api/v1/oauth/token | Device polls for token


# **v1_oauth_device_authorization_create**
> DeviceAuthorizationResponse v1_oauth_device_authorization_create(client_id, device_type, device_os, scope=scope)

Start device authorization (Device Code Flow)

Device posts its metadata and receives a device_code and user_code.

### Example


```python
import transparenc_sdk
from transparenc_sdk.models.device_authorization_response import DeviceAuthorizationResponse
from transparenc_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = transparenc_sdk.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with transparenc_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = transparenc_sdk.OAuthDeviceFlowApi(api_client)
    client_id = 'client_id_example' # str | 
    device_type = 'device_type_example' # str | 
    device_os = 'device_os_example' # str | 
    scope = 'scope_example' # str |  (optional)

    try:
        # Start device authorization (Device Code Flow)
        api_response = api_instance.v1_oauth_device_authorization_create(client_id, device_type, device_os, scope=scope)
        print("The response of OAuthDeviceFlowApi->v1_oauth_device_authorization_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthDeviceFlowApi->v1_oauth_device_authorization_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**|  | 
 **device_type** | **str**|  | 
 **device_os** | **str**|  | 
 **scope** | **str**|  | [optional] 

### Return type

[**DeviceAuthorizationResponse**](DeviceAuthorizationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_oauth_token_create**
> DeviceAuthorizationResponse v1_oauth_token_create(device_token_request)

Device polls for token

Device polls for token

### Example


```python
import transparenc_sdk
from transparenc_sdk.models.device_authorization_response import DeviceAuthorizationResponse
from transparenc_sdk.models.device_token_request import DeviceTokenRequest
from transparenc_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = transparenc_sdk.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with transparenc_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = transparenc_sdk.OAuthDeviceFlowApi(api_client)
    device_token_request = transparenc_sdk.DeviceTokenRequest() # DeviceTokenRequest | 

    try:
        # Device polls for token
        api_response = api_instance.v1_oauth_token_create(device_token_request)
        print("The response of OAuthDeviceFlowApi->v1_oauth_token_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthDeviceFlowApi->v1_oauth_token_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_token_request** | [**DeviceTokenRequest**](DeviceTokenRequest.md)|  | 

### Return type

[**DeviceAuthorizationResponse**](DeviceAuthorizationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

