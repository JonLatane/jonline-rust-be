# Jonline
Federated, open Rust/gRPC social interaction service.

# Build

Requirements: docker, make

## Create Local Docker Registry
Add to `/etc/hosts` (if not already present):

```
127.0.0.1 kubernetes.docker.internal
```

Add to your Docker configuration (in "Docker Engine" settins on macOS):

```json
  "insecure-registries" : ["kubernetes.docker.internal:5000"]
```

The `Makefile` is generally configured to push docker images into the `kubernetes.docker.internal:5000` registry.

Up docker registry:

```
# make create_docker_registry
```

## Build the app
Build:

```
# make
```

# Running locally using docker-compose

## Start dockers

```
# make start
```

## Stop dockers

```
# make stop
```

# Running using kubernetes

## Start pod

```
# make create_pod
```

### Delete pod

```
# make delete_pod
```
