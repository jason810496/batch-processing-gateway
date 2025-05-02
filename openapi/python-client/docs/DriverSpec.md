# DriverSpec


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cores** | **int** |  | [optional] 
**core_request** | **str** |  | [optional] 
**core_limit** | **str** |  | [optional] 
**memory** | **str** |  | [optional] 
**memory_overhead** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**env** | [**List[EnvVar]**](EnvVar.md) |  | [optional] 
**annotations** | **Dict[str, str]** |  | [optional] 

## Example

```python
from bpg_api_client.models.driver_spec import DriverSpec

# TODO update the JSON string below
json = "{}"
# create an instance of DriverSpec from a JSON string
driver_spec_instance = DriverSpec.from_json(json)
# print the JSON string representation of the object
print(DriverSpec.to_json())

# convert the object into a dict
driver_spec_dict = driver_spec_instance.to_dict()
# create an instance of DriverSpec from a dict
driver_spec_from_dict = DriverSpec.from_dict(driver_spec_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


