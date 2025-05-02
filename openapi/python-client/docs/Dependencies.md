# Dependencies


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**jars** | **List[str]** |  | [optional] 
**files** | **List[str]** |  | [optional] 
**py_files** | **List[str]** |  | [optional] 
**packages** | **List[str]** |  | [optional] 
**exclude_packages** | **List[str]** |  | [optional] 
**repositories** | **List[str]** |  | [optional] 
**archives** | **List[str]** |  | [optional] 

## Example

```python
from bpg_api_client.models.dependencies import Dependencies

# TODO update the JSON string below
json = "{}"
# create an instance of Dependencies from a JSON string
dependencies_instance = Dependencies.from_json(json)
# print the JSON string representation of the object
print(Dependencies.to_json())

# convert the object into a dict
dependencies_dict = dependencies_instance.to_dict()
# create an instance of Dependencies from a dict
dependencies_from_dict = Dependencies.from_dict(dependencies_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


