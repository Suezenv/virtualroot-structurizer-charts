# structurizr

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![AppVersion: 3047](https://img.shields.io/badge/AppVersion-3047-informational?style=flat-square)

The Structurizr Helm chart deploys Structurizr On premise flavor. Structurizr is a web-based rendering tool designed to help software development teams create software architecture diagrams and documentation.

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
| image.repository | string | `"structurizr/onpremises"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"structurizr.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` | Specify the number of replicas |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| persistentVolume.enabled | bool | `true` | use persistentVolume |
| persistentVolume.accessModes | list | `[ReadWriteOnce]` | persistentVolume access mode |
| persistentVolume.labels | object | `{}` | add labels  |
| persistentVolume.annotations | object | `{}` | add annotations |
| persistentVolume.existingClaim | string | `` | to use existing claim |
| persistentVolume.size | string | `"8Gi"` | size of persistentVolume |
| persistentVolume.storageClass | string | `"default"` | storage class of persistentVolume |
| persistentVolume.volumeBindingMode | string | `` |  |
| persistentVolume.volumeName | string | `""` |  |




## TODO

- [ ] Encryption
- [ ] Authentication
  - [ ] File
  - [ ] LDAP
  - [ ] SAML
- [ ] Redis sessions
- [ ] Bucket data