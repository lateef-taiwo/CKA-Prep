## Setting up Kind Cluster
Kind (Kubernetes in docker) a tool that will help us to create Kubernetes cluster on top of Docker containers.

    curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/v0.20.0/kind-windows-amd64
    Move-Item .\kind-windows-amd64.exe D:\Kind\kind.exe

On Windows search `Advanced system settings` then Click on `Environment Variables` under `System Variables` set new `Path variable` to `D:\Kind`

Note: you can change the location from `D:\Kind\kind.exe` to whatever you like.

Check the (![kind documentation](https://kind.sigs.k8s.io/docs/user/quick-start/#installation)) for more useful information

The kind.yaml manifest file in this directory can be used to install a kind cluster suitable for local kubernetes testing and also dev/non-prod environments kubernetes cluster setup

### Use the following command to create your kind cluster.
    kind create cluster --config kind.yaml --name my-cluster

To delete the kind cluster, run
    kind delete clusters my-cluster

## For a kubernetes cluster with ingress support, use the following kin-with-ingress-support.yaml config file.
#### Create the Cluster
    kind create cluster --config kind.yaml --name my-cluster
