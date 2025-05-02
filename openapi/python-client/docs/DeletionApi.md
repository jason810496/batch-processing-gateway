# bpg_api_client.DeletionApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_submission**](DeletionApi.md#delete_submission) | **DELETE** /spark/{submissionId} | Delete Spark application by submission ID


# **delete_submission**
> DeleteSubmissionResponse delete_submission(submission_id)

Delete Spark application by submission ID

After a job is submitted, you can use the submission ID returned to delete the job.

### Example


```python
import bpg_api_client
from bpg_api_client.models.delete_submission_response import DeleteSubmissionResponse
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
    api_instance = bpg_api_client.DeletionApi(api_client)
    submission_id = 'submission_id_example' # str | The submission ID returned by submission API

    try:
        # Delete Spark application by submission ID
        api_response = api_instance.delete_submission(submission_id)
        print("The response of DeletionApi->delete_submission:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeletionApi->delete_submission: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **str**| The submission ID returned by submission API | 

### Return type

[**DeleteSubmissionResponse**](DeleteSubmissionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad request due to invalid submission ID or other issues |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

