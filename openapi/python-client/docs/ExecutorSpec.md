# ExecutorSpec


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
**instances** | **int** |  | [optional] 

## Example

```python
from bpg_api_client.models.executor_spec import ExecutorSpec

# TODO update the JSON string below
json = "{}"
# create an instance of ExecutorSpec from a JSON string
executor_spec_instance = ExecutorSpec.from_json(json)
# print the JSON string representation of the object
print(ExecutorSpec.to_json())

# convert the object into a dict
executor_spec_dict = executor_spec_instance.to_dict()
# create an instance of ExecutorSpec from a dict
executor_spec_from_dict = ExecutorSpec.from_dict(executor_spec_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


