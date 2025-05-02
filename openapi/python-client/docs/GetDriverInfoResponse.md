# GetDriverInfoResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pod_name** | **str** |  | [optional] 
**start_time** | **int** |  | [optional] 

## Example

```python
from bpg_api_client.models.get_driver_info_response import GetDriverInfoResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetDriverInfoResponse from a JSON string
get_driver_info_response_instance = GetDriverInfoResponse.from_json(json)
# print the JSON string representation of the object
print(GetDriverInfoResponse.to_json())

# convert the object into a dict
get_driver_info_response_dict = get_driver_info_response_instance.to_dict()
# create an instance of GetDriverInfoResponse from a dict
get_driver_info_response_from_dict = GetDriverInfoResponse.from_dict(get_driver_info_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


