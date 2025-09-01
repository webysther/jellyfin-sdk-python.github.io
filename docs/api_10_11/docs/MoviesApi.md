# jellyfin.generated.api_10_11.MoviesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_movie_recommendations**](MoviesApi.md#get_movie_recommendations) | **GET** /Movies/Recommendations | Gets movie recommendations.


# **get_movie_recommendations**
> List[RecommendationDto] get_movie_recommendations(user_id=user_id, parent_id=parent_id, fields=fields, category_limit=category_limit, item_limit=item_limit)

Gets movie recommendations.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
from jellyfin.generated.api_10_11.models.recommendation_dto import RecommendationDto
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
    api_instance = jellyfin.generated.api_10_11.MoviesApi(api_client)
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    parent_id = 'parent_id_example' # str | Specify this to localize the search to a specific item or folder. Omit to use the root. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. The fields to return. (optional)
    category_limit = 5 # int | The max number of categories to return. (optional) (default to 5)
    item_limit = 8 # int | The max number of items to return per category. (optional) (default to 8)

    try:
        # Gets movie recommendations.
        api_response = api_instance.get_movie_recommendations(user_id=user_id, parent_id=parent_id, fields=fields, category_limit=category_limit, item_limit=item_limit)
        print("The response of MoviesApi->get_movie_recommendations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MoviesApi->get_movie_recommendations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **parent_id** | **str**| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. The fields to return. | [optional] 
 **category_limit** | **int**| The max number of categories to return. | [optional] [default to 5]
 **item_limit** | **int**| The max number of items to return per category. | [optional] [default to 8]

### Return type

[**List[RecommendationDto]**](RecommendationDto.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Movie recommendations returned. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

