# bpg_api_client.SubmissionApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**submit_application**](SubmissionApi.md#submit_application) | **POST** /spark | Submit a Spark application


# **submit_application**
> SubmitApplicationResponse submit_application(submit_application_request, content_type=content_type)

Submit a Spark application

To submit a job, prepare a job payload in the request body either in JSON or YAML format.

### Example


```python
import bpg_api_client
from bpg_api_client.models.submit_application_request import SubmitApplicationRequest
from bpg_api_client.models.submit_application_response import SubmitApplicationResponse
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
    api_instance = bpg_api_client.SubmissionApi(api_client)
    submit_application_request = bpg_api_client.SubmitApplicationRequest() # SubmitApplicationRequest | All the specification of the job, including necessary artifacts, versions, driver and executor specs
    content_type = 'content_type_example' # str | options: application/json, text/yaml, or leave it empty for API to figure out (optional)

    try:
        # Submit a Spark application
        api_response = api_instance.submit_application(submit_application_request, content_type=content_type)
        print("The response of SubmissionApi->submit_application:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubmissionApi->submit_application: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submit_application_request** | [**SubmitApplicationRequest**](SubmitApplicationRequest.md)| All the specification of the job, including necessary artifacts, versions, driver and executor specs | 
 **content_type** | **str**| options: application/json, text/yaml, or leave it empty for API to figure out | [optional] 

### Return type

[**SubmitApplicationResponse**](SubmitApplicationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/yaml
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad request due to wrong format or invalid values |  -  |
**415** | Unsupported content type |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

