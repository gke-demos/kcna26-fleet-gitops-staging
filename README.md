# kcna26-fleet-gitops-staging

Desired state for the staging install of the KubeCon NA 2026 kube-agents demo, where a new
kube-agents release is tried before the demo install moves to it. Config Sync applies
`clusters/<cluster>/` to each cluster; the kube-agents Platform Agent proposes every change as a
pull request here and never writes to a cluster itself. A human merges.

| Cluster        | App                                                                                 |
| -------------- | ----------------------------------------------------------------------------------- |
| `boutique-stg` | [Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo) v0.10.7 |

`clusters/boutique-stg/` is a copy of `boutique-prod` in
[`gke-demos/kcna26-fleet-gitops`](https://github.com/gke-demos/kcna26-fleet-gitops) at its
`baseline` tag, planted misconfigurations included. Do not copy it as a template. The demo's
scripts and runbook are in [`gke-demos/kcna26-kube-agents`](https://github.com/gke-demos/kcna26-kube-agents).
