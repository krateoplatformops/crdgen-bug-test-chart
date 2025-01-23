# CRDGEN bug test chart

This is a template used to test crdgen capabilities.

## Requirements

- Have Krateo PlatformOps installed: https://docs.krateo.io/

## How to install

```sh
kubectl create ns crdgen-bug-test-system
kubectl apply -f https://raw.githubusercontent.com/krateoplatformops/crdgen-bug-test-chart/refs/heads/main/compositiondefinition.yaml
```

### With *Krateo Composable Portal*

#### With custom form

```sh
DATE=$(date +"%Y-%m-%dT%H:%M:%SZ")
curl -sL "https://raw.githubusercontent.com/krateoplatformops/crdgen-bug-test-chart/main/customform.yaml" | sed "s/{{DATE}}/$DATE/" | kubectl apply -f -
```