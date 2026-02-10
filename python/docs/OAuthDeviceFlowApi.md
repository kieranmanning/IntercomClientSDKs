# openapi_client.OAuthDeviceFlowApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_oauth_device_authorization_create**](OAuthDeviceFlowApi.md#v1_oauth_device_authorization_create) | **POST** /api/v1/oauth/device-authorization/ | Start device authorization (Device Code Flow)
[**v1_oauth_token_create**](OAuthDeviceFlowApi.md#v1_oauth_token_create) | **POST** /api/v1/oauth/token | Device polls for token


# **v1_oauth_device_authorization_create**
> DeviceAuthorizationResponse v1_oauth_device_authorization_create(device_authorization_request)

Start device authorization (Device Code Flow)

Device posts its metadata and receives a device_code and user_code.

### Example


```python
import openapi_client
from openapi_client.models.device_authorization_request import DeviceAuthorizationRequest
from openapi_client.models.device_authorization_response import DeviceAuthorizationResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.OAuthDeviceFlowApi(api_client)
    device_authorization_request = openapi_client.DeviceAuthorizationRequest() # DeviceAuthorizationRequest | 

    try:
        # Start device authorization (Device Code Flow)
        api_response = api_instance.v1_oauth_device_authorization_create(device_authorization_request)
        print("The response of OAuthDeviceFlowApi->v1_oauth_device_authorization_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthDeviceFlowApi->v1_oauth_device_authorization_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_authorization_request** | [**DeviceAuthorizationRequest**](DeviceAuthorizationRequest.md)|  | 

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

# **v1_oauth_token_create**
> DeviceAuthorizationResponse v1_oauth_token_create(device_token_request)

Device polls for token

Device polls for token

### Example


```python
import openapi_client
from openapi_client.models.device_authorization_response import DeviceAuthorizationResponse
from openapi_client.models.device_token_request import DeviceTokenRequest
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.OAuthDeviceFlowApi(api_client)
    device_token_request = openapi_client.DeviceTokenRequest() # DeviceTokenRequest | 

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

