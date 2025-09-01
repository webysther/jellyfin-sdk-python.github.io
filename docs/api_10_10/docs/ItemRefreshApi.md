# jellyfin.generated.api_10_10.ItemRefreshApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**refresh_item**](ItemRefreshApi.md#refresh_item) | **POST** /Items/{itemId}/Refresh | Refreshes metadata for an item.


# **refresh_item**
> refresh_item(item_id, metadata_refresh_mode=metadata_refresh_mode, image_refresh_mode=image_refresh_mode, replace_all_metadata=replace_all_metadata, replace_all_images=replace_all_images)

Refreshes metadata for an item.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_10
from jellyfin.generated.api_10_10 import ApiClient, Configuration
from jellyfin.generated.api_10_10.models.metadata_refresh_mode import MetadataRefreshMode
from jellyfin.generated.api_10_10.rest import ApiException
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
    api_instance = jellyfin.generated.api_10_10.ItemRefreshApi(api_client)
    item_id = 'item_id_example' # str | Item id.
    metadata_refresh_mode = jellyfin.generated.api_10_10.MetadataRefreshMode() # MetadataRefreshMode | (Optional) Specifies the metadata refresh mode. (optional)
    image_refresh_mode = jellyfin.generated.api_10_10.MetadataRefreshMode() # MetadataRefreshMode | (Optional) Specifies the image refresh mode. (optional)
    replace_all_metadata = False # bool | (Optional) Determines if metadata should be replaced. Only applicable if mode is FullRefresh. (optional) (default to False)
    replace_all_images = False # bool | (Optional) Determines if images should be replaced. Only applicable if mode is FullRefresh. (optional) (default to False)

    try:
        # Refreshes metadata for an item.
        api_instance.refresh_item(item_id, metadata_refresh_mode=metadata_refresh_mode, image_refresh_mode=image_refresh_mode, replace_all_metadata=replace_all_metadata, replace_all_images=replace_all_images)
    except Exception as e:
        print("Exception when calling ItemRefreshApi->refresh_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| Item id. | 
 **metadata_refresh_mode** | [**MetadataRefreshMode**](.md)| (Optional) Specifies the metadata refresh mode. | [optional] 
 **image_refresh_mode** | [**MetadataRefreshMode**](.md)| (Optional) Specifies the image refresh mode. | [optional] 
 **replace_all_metadata** | **bool**| (Optional) Determines if metadata should be replaced. Only applicable if mode is FullRefresh. | [optional] [default to False]
 **replace_all_images** | **bool**| (Optional) Determines if images should be replaced. Only applicable if mode is FullRefresh. | [optional] [default to False]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase"

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Item metadata refresh queued. |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Item to refresh not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

