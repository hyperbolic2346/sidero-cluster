# home-infra

My personal k8s cluster built with Sidero and managed by Flux2 GitOps

Very much inspired by and copied mostly from [Charlie Haley's Home Infra](https://github.com/charlie-haley/home-infra)

## 💻 Management Cluster
| Node                     | RAM  | Storage                    | Function           | Operating System     | Quantity
| ------------------------ |------| -------------------------- | ------------------ | -------------------- | --------
| NUC 11 Celeron N5105     | 8GB  | 256GB NVME                 | Sidero CP + Worker | Talos 1.2.7          | 1


## 💻 Blookums Workload Cluster
| Node                     | RAM  | Storage                    | Function           | Operating System     | Quantity
| ------------------------ |------| -------------------------- | ------------------ | -------------------- | --------
| Work-PC                  | 4GB  | 256GB NVME                 | Kube Control Plane | Talos 1.1.2          | 1
| Thing1 Supermicro X10DRT | 64GB | 64GB NVME + 2 * 3TB HDD    | Kube Worker        | Talos 1.1.2          | 1
|                          |      | 2 * 1TB SSD + 4TB HDD      |                    |                      |
| Thing2 Supermicro X10DRT | 64GB | 64GB NVME + 5 * 3TB HDD    | Kube Worker        | Talos 1.1.2          | 1
|                          |      | 1TB SSD                    |                    |                      |

## Cluster

- PXE Boot Talos managed by Sidero
- nginx Ingress
- Rook Ceph
- Prometheus/Grafana/Loki Monitoring Stack

## 🦾 Automations
- [Renovate](https://github.com/renovatebot/renovate)
- [GitHub Action YAMLlint](https://github.com/ibiqlik/action-yamllint)
- [Renovate Helm Releases](https://github.com/k8s-at-home/renovate-helm-releases)
