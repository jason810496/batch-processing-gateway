# SubmitApplicationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**submission_id** | **str** |  | [optional] 

## Example

```python
from bpg_api_client.models.submit_application_response import SubmitApplicationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SubmitApplicationResponse from a JSON string
submit_application_response_instance = SubmitApplicationResponse.from_json(json)
# print the JSON string representation of the object
print(SubmitApplicationResponse.to_json())

# convert the object into a dict
submit_application_response_dict = submit_application_response_instance.to_dict()
# create an instance of SubmitApplicationResponse from a dict
submit_application_response_from_dict = SubmitApplicationResponse.from_dict(submit_application_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


