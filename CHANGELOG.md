# Changes in DockerSpawner

## 0.4

- get singleuser scipt from jupyterhub 0.6.1 (0.7 will require jupyterhub package to run singleuser script)
- `get_ip_and_port()` is a tornado coroutine, rather than an asyncio coroutine, for consistency with the rest of the code.
- more configuration for ports and mounts

## 0.3

- Moved to jupyterhub org (`jupyterhub/singleuser`, `jupyterhub/systemuser` on Docker)
- Add `rebase-singleuser` tool for building new single-user images on top of different bases
- Base default docker images on `jupyter/scipy-notebook` from jupyter/docker-stacks
- Fix environment setup to use `get_env` instead of `_env_default` (Needed for JupyterHub 0.5)

## 0.2

- Add `DockerSpawner.links` 
- Use HostIp from docker port output
- Make user home string template configurable

## 0.1

First release