# kubernetes-operator-dgraph

kubernetes-operator-dgraph is a Kubernetes operator built with [operator-sdk](https://sdk.operatorframework.io/) and [the official Dgraph Helm charts](https://github.com/dgraph-io/charts). It aims to simplify deployments of Dgraph clusters by abstracting away the Kubernetes resources behind a custom resource definition.

Many resources use the namespace `roshanbhatia.com` to signify that this is a community-driven project, not an official one.

## Prerequisites

Before getting started, ensure that you have the following dependencies installed on your system:

- Docker - [Installation Guide](https://docs.docker.com/get-docker/)
- Kubernetes (Kind) - [Installation Guide](https://kind.sigs.k8s.io/)

## Getting Started

1. Create a local kind cluster using the following command:

```bash
make create-kind-cluster
```

2. Build the operator's docker image.

```bash
make docker-build
```

3. Load the image into the kind cluster:

```bash
make load-image-to-kind
```

4. Deploy the docker image to kind:

```bash
make deploy
```

4. Deploy the Dgraph custom resource sample to kind:

```bash
make deploy-sample-to-kind
```

To clean up the kind cluster resources, use the following command:

```bash
make reset-kind-cluster
```

## Attributions

As stated above, this was built with:

- [operator-sdk](https://sdk.operatorframework.io/)
- [Official Dgraph Helm charts](https://github.com/dgraph-io/charts)
