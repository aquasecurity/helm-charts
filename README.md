![Aquasecurity logo](https://avatars3.githubusercontent.com/u/12783832?s=200&v=4)
# Aqua Security Helm Charts

[![License][license-img]][license]

[license-img]: https://img.shields.io/badge/License-Apache%202.0-blue.svg
[license]: https://github.com/aquasecurity/helm-charts/blob/master/LICENSE

Aqua Security Open Source Projects Helm Charts on a [Kubernetes](https://kubernetes.io) cluster using the
[Helm](https://helm.sh) package manager.

## Charts

- [Trivy Operator](https://github.com/aquasecurity/trivy-operator/tree/main/deploy/helm)
- [Starboard](https://github.com/aquasecurity/starboard/tree/main/deploy/helm)
- [Trivy](https://github.com/aquasecurity/trivy/tree/main/helm/trivy)

## Prerequisites

- Kubernetes 1.15+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure

#### Installing [Helm](https://helm.sh)

```
curl -L https://git.io/get_helm.sh | bash
helm init
```

## Installing Aqua Community Helm Repository

```
helm repo add aquasecurity https://aquasecurity.github.io/helm-charts/
helm repo update
```

## Installing the Chart

Search all the repositories available
```
helm search repo aquasecurity -l
```

Install specific helm chart
```
helm install starboard aquasecurity/starboard-operator
helm status starboard
```

## Uninstalling the Chart

To uninstall/delete the `starboard` deployment:

```
$ helm delete starboard
```