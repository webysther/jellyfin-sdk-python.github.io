# jellyfin.generated.api_10_10.ApiKeyApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_key**](ApiKeyApi.md#create_key) | **POST** /Auth/Keys | Create a new api key.
[**get_keys**](ApiKeyApi.md#get_keys) | **GET** /Auth/Keys | Get all keys.
[**revoke_key**](ApiKeyApi.md#revoke_key) | **DELETE** /Auth/Keys/{key} | Remove an api key.


# **create_key**
> create_key(app)

Create a new api key.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_10
from jellyfin.generated.api_10_10 import ApiClient, Configuration
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
    api_instance = jellyfin.generated.api_10_10.ApiKeyApi(api_client)
    app = 'app_example' # str | Name of the app using the authentication key.

    try:
        # Create a new api key.
        api_instance.create_key(app)
    except Exception as e:
        print("Exception when calling ApiKeyApi->create_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **str**| Name of the app using the authentication key. | 

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Api key created. |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_keys**
> AuthenticationInfoQueryResult get_keys()

Get all keys.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_10
from jellyfin.generated.api_10_10 import ApiClient, Configuration
from jellyfin.generated.api_10_10.models.authentication_info_query_result import AuthenticationInfoQueryResult
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
    api_instance = jellyfin.generated.api_10_10.ApiKeyApi(api_client)

    try:
        # Get all keys.
        api_response = api_instance.get_keys()
        print("The response of ApiKeyApi->get_keys:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApiKeyApi->get_keys: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AuthenticationInfoQueryResult**](AuthenticationInfoQueryResult.md)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile="CamelCase", application/json; profile="PascalCase"

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Api keys retrieved. |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_key**
> revoke_key(key)

Remove an api key.

### Example

* Api Key Authentication (CustomAuthentication):

```python
import jellyfin.generated.api_10_10
from jellyfin.generated.api_10_10 import ApiClient, Configuration
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
    api_instance = jellyfin.generated.api_10_10.ApiKeyApi(api_client)
    key = 'key_example' # str | The access token to delete.

    try:
        # Remove an api key.
        api_instance.revoke_key(key)
    except Exception as e:
        print("Exception when calling ApiKeyApi->revoke_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**| The access token to delete. | 

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Api key deleted. |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

