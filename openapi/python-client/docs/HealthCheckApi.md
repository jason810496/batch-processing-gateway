# bpg_api_client.HealthCheckApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**healthcheck_status**](HealthCheckApi.md#healthcheck_status) | **GET** /healthcheck/status | Check the current service status


# **healthcheck_status**
> HealthcheckResponse healthcheck_status()

Check the current service status

### Example


```python
import bpg_api_client
from bpg_api_client.models.healthcheck_response import HealthcheckResponse
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
    api_instance = bpg_api_client.HealthCheckApi(api_client)

    try:
        # Check the current service status
        api_response = api_instance.healthcheck_status()
        print("The response of HealthCheckApi->healthcheck_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthCheckApi->healthcheck_status: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthcheckResponse**](HealthcheckResponse.md)

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

