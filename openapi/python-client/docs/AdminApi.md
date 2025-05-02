# bpg_api_client.AdminApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_submissions**](AdminApi.md#list_submissions) | **GET** /admin/submissions | List submissions from all users
[**version**](AdminApi.md#version) | **GET** /admin/version | Show the version


# **list_submissions**
> str list_submissions(name=name)

List submissions from all users

### Example


```python
import bpg_api_client
from bpg_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = bpg_api_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with bpg_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = bpg_api_client.AdminApi(api_client)
    name = 'name_example' # str | specify this to list only submissions under one application name (optional)

    try:
        # List submissions from all users
        api_response = api_instance.list_submissions(name=name)
        print("The response of AdminApi->list_submissions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdminApi->list_submissions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| specify this to list only submissions under one application name | [optional] 

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **version**
> str version()

Show the version

### Example


```python
import bpg_api_client
from bpg_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = bpg_api_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with bpg_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = bpg_api_client.AdminApi(api_client)

    try:
        # Show the version
        api_response = api_instance.version()
        print("The response of AdminApi->version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdminApi->version: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

