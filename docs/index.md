<h1 align="center">Jellyfin SDK for Python</h1>

---

A High-level Wrapper for OpenAPI Generated Bindings for Jellyfin API.

```sh
pip install jellyfin-sdk
```

```python
import jellyfin

api = jellyfin.api('https://jellyfin.example.com', 'API_TOKEN')

print(api.system.info.version, api.system.info.server_name)
```

- <a href="https://github.com/webysther/jellyfin-sdk-python#usage" target="_blank">Usage</a>
- [SDK Reference](./sdk.md)
- [Jellyfin API 10.10](./api_10_10/README.md) (Stable)
- [Jellyfin API 10.11](./api_10_11/README.md) (Release Candidate)