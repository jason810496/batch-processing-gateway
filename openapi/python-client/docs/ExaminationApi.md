# bpg_api_client.ExaminationApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**describe**](ExaminationApi.md#describe) | **GET** /spark/{submissionId}/describe | Get spark application spec and related events as a text stream.
[**get_driver_info**](ExaminationApi.md#get_driver_info) | **GET** /spark/{submissionId}/driver | Get Spark application driver information.
[**get_log**](ExaminationApi.md#get_log) | **GET** /log | Get driver/executor stdout logs from EKS
[**get_spark_spec**](ExaminationApi.md#get_spark_spec) | **GET** /spark/{submissionId}/spec | Get Spark application spec by submission ID.
[**get_status**](ExaminationApi.md#get_status) | **GET** /spark/{submissionId}/status | Get Spark application status by submission ID.


# **describe**
> str describe(submission_id, client_version=client_version, user=user)

Get spark application spec and related events as a text stream.

May return an empty stream when the Spark application has not started yet.

### Example


```python
import bpg_api_client
from bpg_api_client.models.user import User
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
    api_instance = bpg_api_client.ExaminationApi(api_client)
    submission_id = 'submission_id_example' # str | 
    client_version = 'none' # str |  (optional) (default to 'none')
    user = bpg_api_client.User() # User |  (optional)

    try:
        # Get spark application spec and related events as a text stream.
        api_response = api_instance.describe(submission_id, client_version=client_version, user=user)
        print("The response of ExaminationApi->describe:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExaminationApi->describe: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **str**|  | 
 **client_version** | **str**|  | [optional] [default to &#39;none&#39;]
 **user** | [**User**](User.md)|  | [optional] 

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad request due to invalid submission ID or other issues |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_driver_info**
> GetDriverInfoResponse get_driver_info(submission_id)

Get Spark application driver information.

May return an empty object when the Spark application has not started yet.

### Example


```python
import bpg_api_client
from bpg_api_client.models.get_driver_info_response import GetDriverInfoResponse
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
    api_instance = bpg_api_client.ExaminationApi(api_client)
    submission_id = 'submission_id_example' # str | 

    try:
        # Get Spark application driver information.
        api_response = api_instance.get_driver_info(submission_id)
        print("The response of ExaminationApi->get_driver_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExaminationApi->get_driver_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **str**|  | 

### Return type

[**GetDriverInfoResponse**](GetDriverInfoResponse.md)

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

# **get_log**
> str get_log(sub_id=sub_id, app_id=app_id, exec_id=exec_id)

Get driver/executor stdout logs from EKS

By default driver logs will be returned, unless executor ID is specified.

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
    api_instance = bpg_api_client.ExaminationApi(api_client)
    sub_id = '' # str | submission ID (mutual exclusive with application ID) (optional) (default to '')
    app_id = '' # str | application ID (mutual exclusive with submission ID) (optional) (default to '')
    exec_id = '' # str | If execId is specified, logs from specific executor will be returned. Otherwise driver log will be returned. (optional) (default to '')

    try:
        # Get driver/executor stdout logs from EKS
        api_response = api_instance.get_log(sub_id=sub_id, app_id=app_id, exec_id=exec_id)
        print("The response of ExaminationApi->get_log:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExaminationApi->get_log: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sub_id** | **str**| submission ID (mutual exclusive with application ID) | [optional] [default to &#39;&#39;]
 **app_id** | **str**| application ID (mutual exclusive with submission ID) | [optional] [default to &#39;&#39;]
 **exec_id** | **str**| If execId is specified, logs from specific executor will be returned. Otherwise driver log will be returned. | [optional] [default to &#39;&#39;]

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad request due to invalid submission ID, app ID or other issues |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_spark_spec**
> SparkApplicationSpec get_spark_spec(submission_id)

Get Spark application spec by submission ID.

Return the detailed spec of the Spark job.

### Example


```python
import bpg_api_client
from bpg_api_client.models.spark_application_spec import SparkApplicationSpec
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
    api_instance = bpg_api_client.ExaminationApi(api_client)
    submission_id = 'submission_id_example' # str | 

    try:
        # Get Spark application spec by submission ID.
        api_response = api_instance.get_spark_spec(submission_id)
        print("The response of ExaminationApi->get_spark_spec:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExaminationApi->get_spark_spec: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **str**|  | 

### Return type

[**SparkApplicationSpec**](SparkApplicationSpec.md)

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

# **get_status**
> GetSubmissionStatusResponse get_status(submission_id)

Get Spark application status by submission ID.

May return an empty object when the Spark application is not be started yet.

### Example


```python
import bpg_api_client
from bpg_api_client.models.get_submission_status_response import GetSubmissionStatusResponse
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
    api_instance = bpg_api_client.ExaminationApi(api_client)
    submission_id = 'submission_id_example' # str | 

    try:
        # Get Spark application status by submission ID.
        api_response = api_instance.get_status(submission_id)
        print("The response of ExaminationApi->get_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExaminationApi->get_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **str**|  | 

### Return type

[**GetSubmissionStatusResponse**](GetSubmissionStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad request due to wrong format or invalid values |  -  |
**415** | Unsupported content type |  -  |
**500** | Internal server error |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

