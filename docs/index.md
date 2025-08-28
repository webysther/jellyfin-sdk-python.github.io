<h1 align="center">jellyfin-sdk-python</h1>

---

## Documentation

- [Jellyfin API 10.11](./api_10_11/)
- [Jellyfin API 10.10](./api_10_10/)

A [Possible Official](https://jellyfin.org/docs/general/contributing/branding) Python SDK for Jellyfin.

> Warning: This project is under active development, so API changes may occur.

## Install

```sh
pip install jellyfin-sdk
```

or

```sh
uv add jellyfin-sdk
```

## Usage

### Drop-in replacement for [jellyfin-apiclient-python](https://github.com/jellyfin/jellyfin-apiclient-python)

This library inject the old legacy (almost not maintained) for help migration:

```python
# from
from jellyfin_apiclient_python import JellyfinClient
from jellyfin_apiclient_python.api import API

# to 
from jellyfin.legacy import JellyfinClient
from jellyfin.legacy.api import API
```

### Login

Let's start with login, most cases you only need do something simple:

```python
import os

os.environ["JELLYFIN_URL"] = "https://jellyfin.example.com"
os.environ["JELLYFIN_API_KEY"] = "MY_TOKEN"
```

#### Legacy ([jellyfin-apiclient-python](https://github.com/jellyfin/jellyfin-apiclient-python))

```python
from jellyfin.legacy import JellyfinClient
client = JellyfinClient()
client.authenticate(
    {"Servers": [{
        "AccessToken": os.getenv("JELLYFIN_API_KEY"), 
        "address": os.getenv("JELLYFIN_URL")
    }]}, 
    discover=False
)
system_info = client.jellyfin.get_system_info()

print(system_info.get("Version"), system_info.get("ServerName"))
```

#### Generated Binding with OpenAPI Specification

```python
from jellyfin.generated.api_10_10 import Configuration, ApiClient, SystemApi

client = ApiClient(
    Configuration(host = os.getenv("JELLYFIN_URL")), 
    header_name='X-Emby-Token', 
    header_value=os.getenv("JELLYFIN_API_KEY")
)
system_info = SystemApi(client).get_system_info()

print(system_info.version, system_info.server_name)
```

#### New

```python
import jellyfin

api = jellyfin.api(os.getenv("JELLYFIN_URL"), os.getenv("JELLYFIN_API_KEY"))

print(api.system.info.version, api.system.info.server_name)
```

### Supported Jellyfin Versions

| SDK Version | Jellyfin API Target |
|:-:|:-:|
| 0.1.0 | 10.10.x-10.11.x |
