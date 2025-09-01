<a id="jellyfin"></a>

# jellyfin

Entrypoint module for the Jellyfin SDK.

<a id="jellyfin.api"></a>

#### jellyfin.api

```python
def api(url: str, api_key: str, version: Version = Version.V10_10) -> Api
```

Create an instance of the Jellyfin API client.

**Arguments**:

- `url` _str_ - The base URL of the Jellyfin server.
- `api_key` _str_ - The API key for authentication.
- `version` _Version_ - The API version to use (default is Version.V10_10).
  

**Returns**:

- `Api` - An instance of the Api class.

<a id="jellyfin.api"></a>

# jellyfin.api

Module `api` - High-level interface for ApiClient and Configuration.

<a id="jellyfin.api.Version"></a>

## jellyfin.api.Version Objects

```python
class Version(StrEnum)
```

Enumeration of supported Jellyfin API versions.

<a id="jellyfin.api.Inject"></a>

## jellyfin.api.Inject Objects

```python
class Inject()
```

<a id="jellyfin.api.Inject.get"></a>

#### get

```python
@staticmethod
def get(version: Version)
```

Dynamically imports the appropriate API module based on the specified version.

**Arguments**:

- `version` _Version_ - The API version to import.
  

**Returns**:

- `module` - The imported module corresponding to the specified version.

<a id="jellyfin.api.Api"></a>

## jellyfin.api.Api Objects

```python
class Api()
```

<a id="jellyfin.api.Api.__init__"></a>

#### \_\_init\_\_

```python
def __init__(url: str, api_key: str, version: Version = Version.V10_10)
```

Initializes the Jellyfin API client.

**Arguments**:

- `url` _str_ - The base URL of the Jellyfin server.
- `api_key` _str_ - The API key for authentication.
- `version` _Version_ - The API version to use (default is Version.V10_10).
  

**Raises**:

- `ValueError` - If an unsupported version is provided.
  

**Returns**:

- `Api` - An instance of the Api class.

<a id="jellyfin.api.Api.system"></a>

#### system

```python
@property
def system() -> System
```

Lazy load the System API.

**Returns**:

- `System` - An instance of the System API wrapper.

<a id="jellyfin.api.Api.items"></a>

#### items

```python
@property
def items() -> Items
```

Lazy load the Items API.

**Returns**:

- `Items` - An instance of the Items API wrapper.

<a id="jellyfin.api.Api.user"></a>

#### user

```python
@property
def user() -> User
```

Lazy load the User API.

**Returns**:

- `User` - An instance of the User API wrapper.

<a id="jellyfin.user"></a>

# jellyfin.user

Module `user` - High-level interface for UserApi and UserViewsApi.

<a id="jellyfin.user.User"></a>

## jellyfin.user.User Objects

```python
class User()
```

<a id="jellyfin.user.User.__init__"></a>

#### \_\_init\_\_

```python
def __init__(user_api: object, user_views_api: object)
```

Initializes the User API wrapper.

**Arguments**:

- `user_api` _UserApi_ - An instance of the generated UserApi class.
- `user_views_api` _UserViewsApi_ - An instance of the generated UserViewsApi class.

<a id="jellyfin.user.User.of"></a>

#### of

```python
def of(user_uuid: str | uuid.UUID) -> 'User'
```

Set user context

**Arguments**:

- `user_uuid` _str | uuid.UUID_ - The UUID or name of the user.
  

**Raises**:

- `ValueError` - If the provided user_uuid is not a valid UUID or name.
  

**Returns**:

- `User` - The current User instance with the user context set.

<a id="jellyfin.user.User.by_id"></a>

#### by\_id

```python
def by_id(user_id: uuid.UUID) -> object
```

Get user by ID

**Arguments**:

- `user_id` _uuid.UUID_ - The UUID of the user.
  

**Returns**:

- `UserDto` - The user object if found.

<a id="jellyfin.user.User.by_name"></a>

#### by\_name

```python
def by_name(user_name: str, sensitive: bool = False)
```

Get user by name

<a id="jellyfin.user.User.users"></a>

#### users

```python
@property
def users() -> object
```

Get all users.

**Returns**:

- `UserApi.get_users` - A list of all users.

<a id="jellyfin.user.User.all"></a>

#### all

```python
@property
def all() -> object
```

Get all users. Alias for users

**Returns**:

- `UserApi.get_users` - A list of all users.

<a id="jellyfin.user.User.libraries"></a>

#### libraries

```python
@property
def libraries() -> object
```

Get libraries. Alias for views

**Returns**:

- `BaseItemDtoQueryResult` - A list of libraries.

<a id="jellyfin.user.User.views"></a>

#### views

```python
@property
def views() -> object
```

Get libraries for the current user context.

**Raises**:

- `ValueError` - If user ID is not set.
  

**Returns**:

- `BaseItemDtoQueryResult` - A list of libraries.

<a id="jellyfin.user.User.get_libraries"></a>

#### get\_libraries

```python
def get_libraries(user_id: str | uuid.UUID) -> object
```

Get libraries for a specific user.

**Arguments**:

- `user_id` _str | uuid.UUID_ - The UUID of the user.
  

**Returns**:

- `BaseItemDtoQueryResult` - A list of libraries.

<a id="jellyfin.user.User.__getattr__"></a>

#### \_\_getattr\_\_

```python
def __getattr__(name)
```

Delegate attribute access to user_api, user_views_api, or the current user object.

<a id="jellyfin.items"></a>

# jellyfin.items

Module `items` - High-level interface for ItemsApi.

<a id="jellyfin.items.Items"></a>

## jellyfin.items.Items Objects

```python
class Items()
```

<a id="jellyfin.items.Items.__init__"></a>

#### \_\_init\_\_

```python
def __init__(items_api: object)
```

Initializes the Items API wrapper.

**Arguments**:

- `items_api` _ItemsApi_ - An instance of the generated ItemsApi class.

<a id="jellyfin.items.Items.all"></a>

#### all

```python
@property
def all() -> object
```

Returns all items.

**Returns**:

- `BaseItemDtoQueryResult` - A list of all items.

<a id="jellyfin.items.Items.filter"></a>

#### filter

```python
@property
def filter() -> object
```

Returns a filtered list of items.

**Returns**:

- `ItemsApi.get_items` - A filtered list of items.

<a id="jellyfin.system"></a>

# jellyfin.system

Module `system` - High-level interface for SystemAPI.

<a id="jellyfin.system.System"></a>

## jellyfin.system.System Objects

```python
class System()
```

<a id="jellyfin.system.System.__init__"></a>

#### \_\_init\_\_

```python
def __init__(system_api: object)
```

Initializes the System API wrapper.

**Arguments**:

- `system_api` _SystemApi_ - An instance of the generated SystemApi class.

<a id="jellyfin.system.System.info"></a>

#### info

```python
@property
def info()
```

Returns system information.

**Returns**:

- `SystemInfo` - System information.

