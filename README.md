# Cached build

Version: 1.0.1

Assuming a top-level Dockerfile and docker-compose, build cached images to the current repo register

## Usage

```yaml

- uses: mysociety/cached-build-action@b82a169a68294951c527b14e138771e69c8c492f # v1.0.1
  id: example-step 
  with:
    registry: 'ghcr.io'  # default
    github_token: '' 
    branch: '' 
    docker_compose_file: 'docker-compose.yml'  # default
    docker_compose_file_app: 'app'  # default
    dockerfile: 'Dockerfile'  # default
    push_to_registry: 'true'  # default

```

## Inputs

### registry

Required.

Registry to upload to (default ghcr.io)

Default: ghcr.io

### github_token

Authenticated github token for this repo

### branch

Required.

Should be github.ref_name

### docker_compose_file

Required.

Docker-compose file to build app

Default: docker-compose.yml

### docker_compose_file_app

Required.

App to build in docker compose

Default: app

### dockerfile

Required.

If multi-stage build, needed to extract the base image

Default: Dockerfile

### push_to_registry

Boolean if building should also push to registry

Default: true

