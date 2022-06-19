# rust-grpc-example
Rust grpc client/server example using diesel and postgresql.

# Build

Requirements: docker, make

Add to `/etc/hosts` file:

```
127.0.0.1 kubernetes.docker.internal
```

Make push docker images into the `kubernetes.docker.internal:5000` registry.

Up docker registry:

```
# make create_docker_registry
```

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
