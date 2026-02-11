# OAuthDeviceFlowAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1OauthDeviceAuthorizationCreate**](OAuthDeviceFlowAPI.md#v1oauthdeviceauthorizationcreate) | **POST** /api/v1/oauth/device-authorization/ | Start device authorization (Device Code Flow)
[**v1OauthTokenCreate**](OAuthDeviceFlowAPI.md#v1oauthtokencreate) | **POST** /api/v1/oauth/token | Device polls for token


# **v1OauthDeviceAuthorizationCreate**
```swift
    open class func v1OauthDeviceAuthorizationCreate(clientId: String, deviceType: String, deviceOs: String, scope: String? = nil, completion: @escaping (_ data: DeviceAuthorizationResponse?, _ error: Error?) -> Void)
```

Start device authorization (Device Code Flow)

Device posts its metadata and receives a device_code and user_code.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let clientId = "clientId_example" // String | 
let deviceType = "deviceType_example" // String | 
let deviceOs = "deviceOs_example" // String | 
let scope = "scope_example" // String |  (optional)

// Start device authorization (Device Code Flow)
OAuthDeviceFlowAPI.v1OauthDeviceAuthorizationCreate(clientId: clientId, deviceType: deviceType, deviceOs: deviceOs, scope: scope) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientId** | **String** |  | 
 **deviceType** | **String** |  | 
 **deviceOs** | **String** |  | 
 **scope** | **String** |  | [optional] 

### Return type

[**DeviceAuthorizationResponse**](DeviceAuthorizationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1OauthTokenCreate**
```swift
    open class func v1OauthTokenCreate(deviceTokenRequest: DeviceTokenRequest, completion: @escaping (_ data: DeviceAuthorizationResponse?, _ error: Error?) -> Void)
```

Device polls for token

Device polls for token

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let deviceTokenRequest = DeviceTokenRequest(grantType: GrantTypeEnum(), deviceCode: "deviceCode_example", clientId: "clientId_example") // DeviceTokenRequest | 

// Device polls for token
OAuthDeviceFlowAPI.v1OauthTokenCreate(deviceTokenRequest: deviceTokenRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deviceTokenRequest** | [**DeviceTokenRequest**](DeviceTokenRequest.md) |  | 

### Return type

[**DeviceAuthorizationResponse**](DeviceAuthorizationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

