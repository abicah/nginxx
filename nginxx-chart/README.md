# Nginxx Helm Chart

A Helm chart for deploying nginx on Kubernetes.

## Installation

```bash
helm install my-nginxx ./nginxx-chart
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `replicaCount` | int | `2` | Number of nginx replicas |
| `image.repository` | string | `nginx` | Image repository |
| `image.tag` | string | `1.25-alpine` | Image tag |
| `image.pullPolicy` | string | `IfNotPresent` | Image pull policy |
| `service.type` | string | `ClusterIP` | Service type |
| `service.port` | int | `80` | Service port |
| `service.targetPort` | int | `80` | Container port |
| `ingress.enabled` | bool | `true` | Enable ingress |
| `ingress.hosts[0].host` | string | `nginxx.afpa-devops.lab` | Ingress hostname |

## Usage

### Deploy with default values
```bash
helm install my-nginxx ./nginxx-chart
```

### Deploy with custom values
```bash
helm install my-nginxx ./nginxx-chart -f custom-values.yaml
```

### Upgrade release
```bash
helm upgrade my-nginxx ./nginxx-chart
```

### Uninstall release
```bash
helm uninstall my-nginxx
```
