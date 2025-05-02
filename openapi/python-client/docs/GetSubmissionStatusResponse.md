# GetSubmissionStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**creation_time** | **int** |  | [optional] 
**spark_application_id** | **str** |  | [optional] 
**execution_attempts** | **int** |  | [optional] 
**termination_time** | **int** |  | [optional] 
**duration** | **int** |  | [optional] 
**application_state** | **str** |  | [optional] 
**application_error_message** | **str** |  | [optional] 
**spark_ui_url** | **str** |  | [optional] 

## Example

```python
from bpg_api_client.models.get_submission_status_response import GetSubmissionStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubmissionStatusResponse from a JSON string
get_submission_status_response_instance = GetSubmissionStatusResponse.from_json(json)
# print the JSON string representation of the object
print(GetSubmissionStatusResponse.to_json())

# convert the object into a dict
get_submission_status_response_dict = get_submission_status_response_instance.to_dict()
# create an instance of GetSubmissionStatusResponse from a dict
get_submission_status_response_from_dict = GetSubmissionStatusResponse.from_dict(get_submission_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


