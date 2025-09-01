<a id="jellyfin"></a>

# jellyfin

A High-level Wrapper for OpenAPI Generated Bindings for Jellyfin API.

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

Module `api` - Entry point for interacting with the Jellyfin API.

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

- `version`: The API version to import.

**Returns**:

The imported module corresponding to the specified version.

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

An instance of the System API wrapper.

<a id="jellyfin.api.Api.items"></a>

#### items

```python
@property
def items() -> Items
```

Lazy load the Items API.

**Returns**:

An instance of the Items API wrapper.

<a id="jellyfin.api.Api.user"></a>

#### user

```python
@property
def user() -> User
```

Lazy load the User API.

**Returns**:

An instance of the User API wrapper.

<a id="jellyfin.user"></a>

# jellyfin.user

<a id="jellyfin.user.User"></a>

## jellyfin.user.User Objects

```python
class User()
```

<a id="jellyfin.user.User.of"></a>

#### of

```python
def of(user_uuid: str | uuid.UUID)
```

Set user context

<a id="jellyfin.user.User.by_id"></a>

#### by\_id

```python
def by_id(user_id)
```

Get user by ID

<a id="jellyfin.user.User.by_name"></a>

#### by\_name

```python
def by_name(user_name, sensitive=False)
```

Get user by name

<a id="jellyfin.user.User.users"></a>

#### users

```python
@property
def users()
```

Get all users. Alias for all

<a id="jellyfin.user.User.all"></a>

#### all

```python
@property
def all()
```

Get all users

<a id="jellyfin.user.User.libraries"></a>

#### libraries

```python
@property
def libraries()
```

Get libraries. Alias for views

<a id="jellyfin.items"></a>

# jellyfin.items

Module `items` - Manages Items in Jellyfin.

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

- `ItemsApi`: An instance of the generated ItemsApi class.

<a id="jellyfin.items.Items.all"></a>

#### all

```python
@property
def all() -> object
```

Returns all items.

**Returns**:

`BaseItemDtoQueryResult`: A list of all items.

<a id="jellyfin.system"></a>

# jellyfin.system

