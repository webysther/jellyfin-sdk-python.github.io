# jellyfin.generated.api_10_11.StudiosApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_studio**](StudiosApi.md#get_studio) | **GET** /Studios/{name} | Gets a studio by name.
[**get_studios**](StudiosApi.md#get_studios) | **GET** /Studios | Gets all studios from a given item, folder, or the entire library.


# **get_studio**
> BaseItemDto get_studio(name, user_id=user_id)

Gets a studio by name.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11.models.base_item_dto import BaseItemDto
from jellyfin.generated.api_10_11.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = jellyfin.generated.api_10_11.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CustomAuthentication
configuration.api_key['CustomAuthentication'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CustomAuthentication'] = 'Bearer'

# Enter a context with an instance of the API client
with jellyfin.generated.api_10_11.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = jellyfin.generated.api_10_11.StudiosApi(api_client)
    name = 'name_example' # str | Studio name.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)

    try:
        # Gets a studio by name.
        api_response = api_instance.get_studio(name, user_id=user_id)
        print("The response of StudiosApi->get_studio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudiosApi->get_studio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| Studio name. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 

### Return type

[**BaseItemDto**](BaseItemDto.md)

### Authorization

[CustomAuthentication](README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Studio returned. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](README.md#documentation-for-api-endpoints) [[Back to Model list]](README.md#documentation-for-models) [[Back to README]](README.md)

# **get_studios**
> BaseItemDtoQueryResult get_studios(start_index=start_index, limit=limit, search_term=search_term, parent_id=parent_id, fields=fields, exclude_item_types=exclude_item_types, include_item_types=include_item_types, is_favorite=is_favorite, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types, user_id=user_id, name_starts_with_or_greater=name_starts_with_or_greater, name_starts_with=name_starts_with, name_less_than=name_less_than, enable_images=enable_images, enable_total_record_count=enable_total_record_count)

Gets all studios from a given item, folder, or the entire library.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.base_item_kind import BaseItemKind
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
from jellyfin.generated.api_10_11.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = jellyfin.generated.api_10_11.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CustomAuthentication
configuration.api_key['CustomAuthentication'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CustomAuthentication'] = 'Bearer'

# Enter a context with an instance of the API client
with jellyfin.generated.api_10_11.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = jellyfin.generated.api_10_11.StudiosApi(api_client)
    start_index = 56 # int | Optional. The record index to start at. All items with a lower index will be dropped from the results. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    search_term = 'search_term_example' # str | Optional. Search term. (optional)
    parent_id = 'parent_id_example' # str | Specify this to localize the search to a specific item or folder. Omit to use the root. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    exclude_item_types = [jellyfin.generated.api_10_11.BaseItemKind()] # List[BaseItemKind] | Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited. (optional)
    include_item_types = [jellyfin.generated.api_10_11.BaseItemKind()] # List[BaseItemKind] | Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. (optional)
    is_favorite = True # bool | Optional filter by items that are marked as favorite, or not. (optional)
    enable_user_data = True # bool | Optional, include user data. (optional)
    image_type_limit = 56 # int | Optional, the max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)
    user_id = 'user_id_example' # str | User id. (optional)
    name_starts_with_or_greater = 'name_starts_with_or_greater_example' # str | Optional filter by items whose name is sorted equally or greater than a given input string. (optional)
    name_starts_with = 'name_starts_with_example' # str | Optional filter by items whose name is sorted equally than a given input string. (optional)
    name_less_than = 'name_less_than_example' # str | Optional filter by items whose name is equally or lesser than a given input string. (optional)
    enable_images = True # bool | Optional, include image information in output. (optional) (default to True)
    enable_total_record_count = True # bool | Total record count. (optional) (default to True)

    try:
        # Gets all studios from a given item, folder, or the entire library.
        api_response = api_instance.get_studios(start_index=start_index, limit=limit, search_term=search_term, parent_id=parent_id, fields=fields, exclude_item_types=exclude_item_types, include_item_types=include_item_types, is_favorite=is_favorite, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types, user_id=user_id, name_starts_with_or_greater=name_starts_with_or_greater, name_starts_with=name_starts_with, name_less_than=name_less_than, enable_images=enable_images, enable_total_record_count=enable_total_record_count)
        print("The response of StudiosApi->get_studios:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StudiosApi->get_studios: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **search_term** | **str**| Optional. Search term. | [optional] 
 **parent_id** | **str**| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **exclude_item_types** | [**List[BaseItemKind]**](BaseItemKind.md)| Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited. | [optional] 
 **include_item_types** | [**List[BaseItemKind]**](BaseItemKind.md)| Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. | [optional] 
 **is_favorite** | **bool**| Optional filter by items that are marked as favorite, or not. | [optional] 
 **enable_user_data** | **bool**| Optional, include user data. | [optional] 
 **image_type_limit** | **int**| Optional, the max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 
 **user_id** | **str**| User id. | [optional] 
 **name_starts_with_or_greater** | **str**| Optional filter by items whose name is sorted equally or greater than a given input string. | [optional] 
 **name_starts_with** | **str**| Optional filter by items whose name is sorted equally than a given input string. | [optional] 
 **name_less_than** | **str**| Optional filter by items whose name is equally or lesser than a given input string. | [optional] 
 **enable_images** | **bool**| Optional, include image information in output. | [optional] [default to True]
 **enable_total_record_count** | **bool**| Total record count. | [optional] [default to True]

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Studios returned. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](README.md#documentation-for-api-endpoints) [[Back to Model list]](README.md#documentation-for-models) [[Back to README]](README.md)

