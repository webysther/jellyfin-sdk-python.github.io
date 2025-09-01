# jellyfin.generated.api_10_11.MediaSegmentsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_item_segments**](MediaSegmentsApi.md#get_item_segments) | **GET** /MediaSegments/{itemId} | Gets all media segments based on an itemId.


# **get_item_segments**
> MediaSegmentDtoQueryResult get_item_segments(item_id, include_segment_types=include_segment_types)

Gets all media segments based on an itemId.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.media_segment_dto_query_result import MediaSegmentDtoQueryResult
from jellyfin.generated.api_10_11.models.media_segment_type import MediaSegmentType
from jellyfin.generated.api_10_11.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = Configuration(
    host = "http://localhost"
)

# Configure API key authorization: CustomAuthentication
configuration.api_key['CustomAuthentication'] = f'Token="{os.getenv("API_KEY")}"'
configuration.api_key_prefix['CustomAuthentication'] = "MediaBrowser"


# Enter a context with an instance of the API client
with ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = jellyfin.generated.api_10_11.MediaSegmentsApi(api_client)
    item_id = 'item_id_example' # str | The ItemId.
    include_segment_types = [jellyfin.generated.api_10_11.MediaSegmentType()] # List[MediaSegmentType] | Optional filter of requested segment types. (optional)

    try:
        # Gets all media segments based on an itemId.
        api_response = api_instance.get_item_segments(item_id, include_segment_types=include_segment_types)
        print("The response of MediaSegmentsApi->get_item_segments:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaSegmentsApi->get_item_segments: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The ItemId. | 
 **include_segment_types** | [**List[MediaSegmentType]**](MediaSegmentType.md)| Optional filter of requested segment types. | [optional] 

### Return type

[**MediaSegmentDtoQueryResult**](MediaSegmentDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**404** | Not Found |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

