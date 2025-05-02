# SparkApplicationSpec


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**spark_version** | **str** |  | [optional] 
**original_user** | **str** |  | [optional] 
**proxy_user** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**main_class** | **str** |  | [optional] 
**main_application_file** | **str** |  | [optional] 
**arguments** | **List[str]** |  | [optional] 
**annotations** | **Dict[str, str]** |  | [optional] 
**driver** | [**DriverSpec**](DriverSpec.md) |  | [optional] 
**executor** | [**ExecutorSpec**](ExecutorSpec.md) |  | [optional] 
**deps** | [**Dependencies**](Dependencies.md) |  | [optional] 
**python_version** | **str** |  | [optional] 

## Example

```python
from bpg_api_client.models.spark_application_spec import SparkApplicationSpec

# TODO update the JSON string below
json = "{}"
# create an instance of SparkApplicationSpec from a JSON string
spark_application_spec_instance = SparkApplicationSpec.from_json(json)
# print the JSON string representation of the object
print(SparkApplicationSpec.to_json())

# convert the object into a dict
spark_application_spec_dict = spark_application_spec_instance.to_dict()
# create an instance of SparkApplicationSpec from a dict
spark_application_spec_from_dict = SparkApplicationSpec.from_dict(spark_application_spec_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


