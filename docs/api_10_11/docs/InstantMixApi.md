# jellyfin.generated.api_10_11.InstantMixApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_instant_mix_from_album**](InstantMixApi.md#get_instant_mix_from_album) | **GET** /Albums/{itemId}/InstantMix | Creates an instant playlist based on a given album.
[**get_instant_mix_from_artists**](InstantMixApi.md#get_instant_mix_from_artists) | **GET** /Artists/{itemId}/InstantMix | Creates an instant playlist based on a given artist.
[**get_instant_mix_from_artists2**](InstantMixApi.md#get_instant_mix_from_artists2) | **GET** /Artists/InstantMix | Creates an instant playlist based on a given artist.
[**get_instant_mix_from_item**](InstantMixApi.md#get_instant_mix_from_item) | **GET** /Items/{itemId}/InstantMix | Creates an instant playlist based on a given item.
[**get_instant_mix_from_music_genre_by_id**](InstantMixApi.md#get_instant_mix_from_music_genre_by_id) | **GET** /MusicGenres/InstantMix | Creates an instant playlist based on a given genre.
[**get_instant_mix_from_music_genre_by_name**](InstantMixApi.md#get_instant_mix_from_music_genre_by_name) | **GET** /MusicGenres/{name}/InstantMix | Creates an instant playlist based on a given genre.
[**get_instant_mix_from_playlist**](InstantMixApi.md#get_instant_mix_from_playlist) | **GET** /Playlists/{itemId}/InstantMix | Creates an instant playlist based on a given playlist.
[**get_instant_mix_from_song**](InstantMixApi.md#get_instant_mix_from_song) | **GET** /Songs/{itemId}/InstantMix | Creates an instant playlist based on a given song.


# **get_instant_mix_from_album**
> BaseItemDtoQueryResult get_instant_mix_from_album(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given album.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    item_id = 'item_id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given album.
        api_response = api_instance.get_instant_mix_from_album(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_album:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_album: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_artists**
> BaseItemDtoQueryResult get_instant_mix_from_artists(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given artist.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    item_id = 'item_id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given artist.
        api_response = api_instance.get_instant_mix_from_artists(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_artists:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_artists: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_artists2**
> BaseItemDtoQueryResult get_instant_mix_from_artists2(id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given artist.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    id = 'id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given artist.
        api_response = api_instance.get_instant_mix_from_artists2(id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_artists2:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_artists2: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_item**
> BaseItemDtoQueryResult get_instant_mix_from_item(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given item.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    item_id = 'item_id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given item.
        api_response = api_instance.get_instant_mix_from_item(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_item:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_music_genre_by_id**
> BaseItemDtoQueryResult get_instant_mix_from_music_genre_by_id(id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given genre.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    id = 'id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given genre.
        api_response = api_instance.get_instant_mix_from_music_genre_by_id(id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_music_genre_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_music_genre_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_music_genre_by_name**
> BaseItemDtoQueryResult get_instant_mix_from_music_genre_by_name(name, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given genre.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    name = 'name_example' # str | The genre name.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given genre.
        api_response = api_instance.get_instant_mix_from_music_genre_by_name(name, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_music_genre_by_name:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_music_genre_by_name: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The genre name. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_playlist**
> BaseItemDtoQueryResult get_instant_mix_from_playlist(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given playlist.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    item_id = 'item_id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given playlist.
        api_response = api_instance.get_instant_mix_from_playlist(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_playlist:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_playlist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_instant_mix_from_song**
> BaseItemDtoQueryResult get_instant_mix_from_song(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)

Creates an instant playlist based on a given song.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.base_item_dto_query_result import BaseItemDtoQueryResult
from jellyfin.generated.api_10_11.models.image_type import ImageType
from jellyfin.generated.api_10_11.models.item_fields import ItemFields
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
    api_instance = jellyfin.generated.api_10_11.InstantMixApi(api_client)
    item_id = 'item_id_example' # str | The item id.
    user_id = 'user_id_example' # str | Optional. Filter by user id, and attach user data. (optional)
    limit = 56 # int | Optional. The maximum number of records to return. (optional)
    fields = [jellyfin.generated.api_10_11.ItemFields()] # List[ItemFields] | Optional. Specify additional fields of information to return in the output. (optional)
    enable_images = True # bool | Optional. Include image information in output. (optional)
    enable_user_data = True # bool | Optional. Include user data. (optional)
    image_type_limit = 56 # int | Optional. The max number of images to return, per image type. (optional)
    enable_image_types = [jellyfin.generated.api_10_11.ImageType()] # List[ImageType] | Optional. The image types to include in the output. (optional)

    try:
        # Creates an instant playlist based on a given song.
        api_response = api_instance.get_instant_mix_from_song(item_id, user_id=user_id, limit=limit, fields=fields, enable_images=enable_images, enable_user_data=enable_user_data, image_type_limit=image_type_limit, enable_image_types=enable_image_types)
        print("The response of InstantMixApi->get_instant_mix_from_song:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstantMixApi->get_instant_mix_from_song: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **str**| The item id. | 
 **user_id** | **str**| Optional. Filter by user id, and attach user data. | [optional] 
 **limit** | **int**| Optional. The maximum number of records to return. | [optional] 
 **fields** | [**List[ItemFields]**](ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional] 
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] 
 **enable_user_data** | **bool**| Optional. Include user data. | [optional] 
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional] 
 **enable_image_types** | [**List[ImageType]**](ImageType.md)| Optional. The image types to include in the output. | [optional] 

### Return type

[**BaseItemDtoQueryResult**](BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase", text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Instant playlist returned. |  -  |
**404** | Item not found. |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

