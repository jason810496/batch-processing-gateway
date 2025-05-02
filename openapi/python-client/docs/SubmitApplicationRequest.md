# SubmitApplicationRequest

Submit Application Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**submission_id_suffix** | **str** | If specified, the suffix will be appended to the submission ID | [optional] 
**application_name** | **str** | Name of the application. This will help listing submissions under the same application later. | [optional] 
**type** | **str** | Should be: Java / Scala / Python. If not specified, the API will try to figure out by itself. | [optional] 
**image** | **str** |  | [optional] 
**spot_instance** | **bool** | To enable Spot Instance feature that schedules all Spark Executor pods to Spot nodes | [optional] 
**spark_version** | **str** | Spark version in the format of x.y, where x and y are integers. | 
**main_class** | **str** | The main class in the jar provided in mainApplicationFile for a Java/Scala Spark job | [optional] 
**main_application_file** | **str** | For Java/Scala Spark jobs, provide the full path to the jar file. For PySpark jobs, provide the full path to the Python file. | 
**arguments** | **List[str]** |  | [optional] 
**annotations** | **Dict[str, str]** |  | [optional] 
**driver** | [**DriverSpec**](DriverSpec.md) |  | 
**executor** | [**ExecutorSpec**](ExecutorSpec.md) |  | 
**deps** | [**Dependencies**](Dependencies.md) |  | [optional] 
**python_version** | **str** |  | [optional] 
**queue** | **str** | If no queue is specified, a default &#39;poc&#39; queue will be used. | [optional] 

## Example

```python
from bpg_api_client.models.submit_application_request import SubmitApplicationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SubmitApplicationRequest from a JSON string
submit_application_request_instance = SubmitApplicationRequest.from_json(json)
# print the JSON string representation of the object
print(SubmitApplicationRequest.to_json())

# convert the object into a dict
submit_application_request_dict = submit_application_request_instance.to_dict()
# create an instance of SubmitApplicationRequest from a dict
submit_application_request_from_dict = SubmitApplicationRequest.from_dict(submit_application_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


