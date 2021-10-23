# btcpayserver

![Version: 0.1.4](https://img.shields.io/badge/Version-0.1.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.1.2](https://img.shields.io/badge/AppVersion-1.1.2-informational?style=flat-square)

A Helm chart for BTCPayServer

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | postgresql | 10.5.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"btcpayserver/btcpayserver"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt-production"` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"traefik-cert-manager"` |  |
| ingress.annotations."traefik.ingress.kubernetes.io/frontend-entry-points" | string | `"https"` |  |
| ingress.annotations."traefik.ingress.kubernetes.io/redirect-entry-point" | string | `"https"` |  |
| ingress.annotations."traefik.ingress.kubernetes.io/rule-type" | string | `"PathPrefixStrip"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"btcpay.lsd.capital"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.tls[0].hosts[0] | string | `"btcpay.lsd.capital"` |  |
| ingress.tls[0].secretName | string | `"btcpayserver-tls"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.enabled | bool | `true` |  |
| persistence.size | string | `"1Gi"` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresql.postgresqlDatabase | string | `"btcpay"` |  |
| postgresql.postgresqlPassword | string | `""` |  |
| postgresql.postgresqlUsername | string | `"btcpay"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `23000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)