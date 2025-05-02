# bpg_api_client.StorageApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**upload_stream**](StorageApi.md#upload_stream) | **POST** /s3/{name} | Upload an artifact to S3 and save as a S3 object.


# **upload_stream**
> UploadS3Response upload_stream(name, content_length=content_length, content_length2=content_length2, folder=folder)

Upload an artifact to S3 and save as a S3 object.

The content length parameter must be exactly same as the size of the stream. DO NOT upload any sensitive data file.

### Example


```python
import bpg_api_client
from bpg_api_client.models.upload_s3_response import UploadS3Response
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
    api_instance = bpg_api_client.StorageApi(api_client)
    name = 'artifact.jar' # str | name of the artifact without parent folders
    content_length = 56 # int | content length can be provided in either query or header (optional)
    content_length2 = 'content_length_example' # str | content length can be provided in either query or header (optional)
    folder = 'your/folder/' # str | the folder path to which you want to publish the artifact (optional)

    try:
        # Upload an artifact to S3 and save as a S3 object.
        api_response = api_instance.upload_stream(name, content_length=content_length, content_length2=content_length2, folder=folder)
        print("The response of StorageApi->upload_stream:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StorageApi->upload_stream: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| name of the artifact without parent folders | 
 **content_length** | **int**| content length can be provided in either query or header | [optional] 
 **content_length2** | **str**| content length can be provided in either query or header | [optional] 
 **folder** | **str**| the folder path to which you want to publish the artifact | [optional] 

### Return type

[**UploadS3Response**](UploadS3Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**0** | default response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

