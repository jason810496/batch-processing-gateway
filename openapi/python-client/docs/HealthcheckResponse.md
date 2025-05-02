# HealthcheckResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 

## Example

```python
from bpg_api_client.models.healthcheck_response import HealthcheckResponse

# TODO update the JSON string below
json = "{}"
# create an instance of HealthcheckResponse from a JSON string
healthcheck_response_instance = HealthcheckResponse.from_json(json)
# print the JSON string representation of the object
print(HealthcheckResponse.to_json())

# convert the object into a dict
healthcheck_response_dict = healthcheck_response_instance.to_dict()
# create an instance of HealthcheckResponse from a dict
healthcheck_response_from_dict = HealthcheckResponse.from_dict(healthcheck_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


