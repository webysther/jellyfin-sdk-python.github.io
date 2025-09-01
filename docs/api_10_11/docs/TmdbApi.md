# jellyfin.generated.api_10_11.TmdbApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tmdb_client_configuration**](TmdbApi.md#tmdb_client_configuration) | **GET** /Tmdb/ClientConfiguration | Gets the TMDb image configuration options.


# **tmdb_client_configuration**
> ConfigImageTypes tmdb_client_configuration()

Gets the TMDb image configuration options.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_11
from jellyfin.generated.api_10_11 import ApiClient, Configuration
from jellyfin.generated.api_10_11.models.config_image_types import ConfigImageTypes
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
    api_instance = jellyfin.generated.api_10_11.TmdbApi(api_client)

    try:
        # Gets the TMDb image configuration options.
        api_response = api_instance.tmdb_client_configuration()
        print("The response of TmdbApi->tmdb_client_configuration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TmdbApi->tmdb_client_configuration: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ConfigImageTypes**](ConfigImageTypes.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/html

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**503** | The server is currently starting or is temporarily not available. |  * Retry-After - A hint for when to retry the operation in full seconds. <br>  * Message - A short plain-text reason why the server is not available. <br>  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

