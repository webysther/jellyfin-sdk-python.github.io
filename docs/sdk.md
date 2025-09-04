<a id="jellyfin"></a>

# jellyfin

Entrypoint module for the Jellyfin SDK.

<a id="jellyfin.version"></a>

#### jellyfin.version

Now you can use jellyfin.version.V10_11

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

<a id="jellyfin.api.Api.__repr__"></a>

#### \_\_repr\_\_

```python
def __repr__()
```

Official string representation of the Api instance.

<a id="jellyfin.api.Api.__str__"></a>

#### \_\_str\_\_

```python
def __str__()
```

String representation of the Api instance.

<a id="jellyfin.api.Api.configuration"></a>

#### configuration

```python
@property
def configuration() -> Configuration
```

Returns the Configuration instance.

<a id="jellyfin.api.Api.client"></a>

#### client

```python
@property
def client() -> ApiClient
```

Returns the ApiClient instance.

<a id="jellyfin.api.Api.register_client"></a>

#### register\_client

```python
def register_client(client_name: str = None,
                    device_name: str = None,
                    device_id: str = None,
                    device_version: str = None) -> Self
```

Just register this as a client with the server.

**Arguments**:

- `client_name` _str, optional_ - The name of the client application. Defaults to the hostname if not provided.
- `device_name` _str, optional_ - The name of the device. Defaults to the OS name if not provided.
- `device_id` _str, optional_ - The unique identifier for the device. Defaults to the MAC address if not provided.
- `device_version` _str, optional_ - The version of the client application. Defaults to the OS version if not provided.
  

**Returns**:

- `Api` - The current instance of the Api class.

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

<a id="jellyfin.api.Api.libraries"></a>

#### libraries

```python
@property
def libraries() -> Items
```

Alias for items of type COLLECTIONFOLDER.

**Returns**:

- `ItemCollection` - A collection of all libraries.

<a id="jellyfin.api.Api.users"></a>

#### users

```python
@property
def users() -> Users
```

Lazy load the User API.

**Returns**:

- `Users` - An instance of the User API wrapper.

<a id="jellyfin.base"></a>

# jellyfin.base

<a id="jellyfin.base.Pagination"></a>

## jellyfin.base.Pagination Objects

```python
class Pagination(Protocol)
```

Protocol for paginated responses.

<a id="jellyfin.base.Model"></a>

## jellyfin.base.Model Objects

```python
class Model()
```

<a id="jellyfin.base.Model.model"></a>

#### model

```python
@property
def model() -> BaseModel
```

Returns the generated model

<a id="jellyfin.base.Model.__str__"></a>

#### \_\_str\_\_

```python
def __str__() -> str
```

Returns the string representation of the model.

<a id="jellyfin.base.Model.__repr__"></a>

#### \_\_repr\_\_

```python
def __repr__() -> str
```

Returns a detailed string representation of the Item object, with each attribute on a new line.

<a id="jellyfin.base.Model.summary"></a>

#### summary

```python
def summary(empty: bool = False, size: int = 80, limit: int = 100) -> None
```

Prints the simple representation of the model.

**Arguments**:

- `empty` _bool_ - If True, includes all values. If False, omits empty values (None, "", 0, [], {}).

<a id="jellyfin.base.Collection"></a>

## jellyfin.base.Collection Objects

```python
class Collection(Sequence)
```

<a id="jellyfin.base.Collection.__iter__"></a>

#### \_\_iter\_\_

```python
def __iter__()
```

Returns an iterator for the collection.

Usage:
    collection = ItemCollection(...)
    for item in collection:
        print(collection.current)  # Always shows the current item

<a id="jellyfin.base.Collection.model"></a>

#### model

```python
@property
def model() -> Model
```

Returns the reference model.

<a id="jellyfin.base.Collection.data"></a>

#### data

```python
@property
def data() -> List[BaseModel]
```

Returns the reference list of items inside model.

<a id="jellyfin.base.Collection.__len__"></a>

#### \_\_len\_\_

```python
def __len__()
```

Returns the total number of records in the collection.

**Returns**:

- `int` - The total number of records.

<a id="jellyfin.items"></a>

# jellyfin.items

Module `items` - High-level interface for ItemsApi.

<a id="jellyfin.items.ItemSearch"></a>

## jellyfin.items.ItemSearch Objects

```python
class ItemSearch()
```

Based on DataFrame Builder pattern

Usage:
    search = api.items.search
    search.is_movie = False
    search.user_id = "abc"
    result = search.all()

    api.items.search.add(is_movie=False).all()
    api.items.search.filter({
        "is_movie": False, 
        "user_id": "abc"
    }).all()

<a id="jellyfin.items.ItemSearch.__setattr__"></a>

#### \_\_setattr\_\_

```python
def __setattr__(name, value)
```

Set a filter using 'search.attr = value'

**Arguments**:

- `name` _str_ - The name of the attribute to set.
- `value` _Any_ - The value to set the attribute to.

<a id="jellyfin.items.ItemSearch.__getattr__"></a>

#### \_\_getattr\_\_

```python
def __getattr__(name)
```

Get a filter using 'search.attr'

**Arguments**:

- `name` _str_ - The name of the attribute to retrieve.
  

**Returns**:

- `Any` - The value of the specified attribute, or None if not found.

<a id="jellyfin.items.ItemSearch.__delattr__"></a>

#### \_\_delattr\_\_

```python
def __delattr__(name)
```

Remove a filter using 'del search.attr'

**Arguments**:

- `name` _str_ - The name of the attribute to remove.

<a id="jellyfin.items.ItemSearch.add"></a>

#### add

```python
def add(key: str, value: Any) -> Self
```

Add multiple filters at once using 'search.add(attr=value, ...)'

**Arguments**:

- `key` _str_ - The name of the attribute to add.
- `value` _Any_ - The value to set the attribute to.
  

**Returns**:

- `ItemSearch` - The current ItemSearch instance (for chaining).

<a id="jellyfin.items.ItemSearch.remove"></a>

#### remove

```python
def remove(key: str) -> Self
```

Remove multiple filters at once using 'search.remove(attr, ...)'

**Arguments**:

- `key` _str_ - The name of the attribute to remove.
  

**Returns**:

- `ItemSearch` - The current ItemSearch instance (for chaining).

<a id="jellyfin.items.ItemSearch.next_page"></a>

#### next\_page

```python
def next_page() -> ItemCollection
```

Move to the next page of results based on the current pagination settings.

**Returns**:

- `ItemCollection` - A collection of items for the next page.

<a id="jellyfin.items.ItemSearch.paginate"></a>

#### paginate

```python
def paginate(size: int = 100) -> Self
```

Enable pagination.

**Arguments**:

- `size` _int_ - The maximum number of results to return per page. Defaults to 100. Zero turns off pagination.
  

**Returns**:

- `ItemSearch` - The current ItemSearch instance (for chaining).

<a id="jellyfin.items.ItemSearch.all"></a>

#### all

```python
@property
def all() -> ItemCollection
```

Execute the search and return all results as an ItemCollection

**Returns**:

- `ItemCollection` - A collection of items matching the search criteria.

<a id="jellyfin.items.ItemSearch.recursive"></a>

#### recursive

```python
def recursive(flag: bool = True) -> Self
```

Shortcut to enable recursive search

<a id="jellyfin.items.ItemSearch.name_starts_with"></a>

#### name\_starts\_with

```python
def name_starts_with(prefix: str) -> Self
```

Shortcut to filter by name prefix

<a id="jellyfin.items.ItemSearch.only_library"></a>

#### only\_library

```python
def only_library() -> Self
```

Shortcut to filter only libraries (collections)

<a id="jellyfin.items.Items"></a>

## jellyfin.items.Items Objects

```python
class Items()
```

<a id="jellyfin.items.Items.__init__"></a>

#### \_\_init\_\_

```python
def __init__(items_api: ItemsApi)
```

Initializes the Items API wrapper.

**Arguments**:

- `items_api` _ItemsApi_ - An instance of the generated ItemsApi class.

<a id="jellyfin.items.Items.all"></a>

#### all

```python
@property
def all() -> ItemCollection
```

Returns all items as an ItemCollection.

**Returns**:

- `ItemCollection` - A collection of all items.

<a id="jellyfin.items.Items.search"></a>

#### search

```python
@property
def search() -> ItemSearch
```

Returns an ItemSearch instance for building search queries.

**Returns**:

- `ItemSearch` - An instance of ItemSearch for building search queries.

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
def __init__(system_api: SystemApi)
```

Initializes the System API wrapper.

**Arguments**:

- `system_api` _SystemApi_ - An instance of the generated SystemApi class.

<a id="jellyfin.system.System.info"></a>

#### info

```python
@property
def info() -> SystemInfo
```

Returns system information.

**Returns**:

- `SystemInfo` - System information.

<a id="jellyfin.users"></a>

# jellyfin.users

Module `user` - High-level interface for UserApi and UserViewsApi.

<a id="jellyfin.users.Users"></a>

## jellyfin.users.Users Objects

```python
class Users()
```

<a id="jellyfin.users.Users.__init__"></a>

#### \_\_init\_\_

```python
def __init__(user_api: UserApi, user_views_api: UserViewsApi)
```

Initializes the User API wrapper.

**Arguments**:

- `user_api` _UserApi_ - An instance of the generated UserApi class.
- `user_views_api` _UserViewsApi_ - An instance of the generated UserViewsApi class.

<a id="jellyfin.users.Users.of"></a>

#### of

```python
def of(user_name_or_uuid: str | uuid.UUID) -> 'User'
```

Set user context

**Arguments**:

- `user_name_or_uuid` _str | uuid.UUID_ - The UUID or name of the user.
  

**Raises**:

- `ValueError` - If the provided user_name_or_uuid is not a valid UUID or name.
  

**Returns**:

- `User` - The current User instance with the user context set.

<a id="jellyfin.users.Users.by_id"></a>

#### by\_id

```python
def by_id(user_id: uuid.UUID) -> User
```

Get user by ID

**Arguments**:

- `user_id` _uuid.UUID_ - The UUID of the user.
  

**Returns**:

- `User` - The user object if found.

<a id="jellyfin.users.Users.by_name"></a>

#### by\_name

```python
def by_name(user_name: str) -> User | None
```

Get user by name

**Arguments**:

- `user_name` _str_ - The name of the user.
  

**Returns**:

  User | None: The user object if found, otherwise None.

<a id="jellyfin.users.Users.all"></a>

#### all

```python
@property
def all() -> UserCollection
```

Get all users.

**Returns**:

- `UserCollection` - A list of all users.

<a id="jellyfin.users.Users.libraries"></a>

#### libraries

```python
@property
def libraries() -> ItemCollection
```

Get libraries for the current user context.

**Returns**:

- `ItemCollection` - A list of libraries.

<a id="jellyfin.users.Users.views"></a>

#### views

```python
@property
def views() -> ItemCollection
```

Get views for the current user context.

**Raises**:

- `ValueError` - If user ID is not set.
  

**Returns**:

- `ItemCollection` - A list of libraries.

<a id="jellyfin.users.Users.__getattr__"></a>

#### \_\_getattr\_\_

```python
def __getattr__(name)
```

Delegate attribute access to user_api, user_views_api, or the current user object.

