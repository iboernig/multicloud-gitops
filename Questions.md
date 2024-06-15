# Questions

## Validated Pattern

### Vault

1. How to manage credentials for Azure and GCP in Vault
   See https://github.com/validatedpatterns/common/tree/main/ansible/roles/vault_utils#values-secret-file-format
   There is an example for AWS but the format for Azure or GCP is not really documented
   
   NB: This is probably irrelevant, as we will provision and import the clusters before the demo

2. We also need to store secrets for S3 (or compatible bucket on GCP) for Restic as part of this [volsync demo](https://github.com/fc7/volsync-demo/blob/main/pacman-gitops-volsync-restic/external-secret-restic-secret.yaml).

### Policies

1. Policy for ArgoCD on K8s (AKS) with [ArgoCD operator installed](https://argocd-operator.readthedocs.io/en/stable/install/olm/#operator-lifecycle-manager) -- would it work?

## VolSync

1. [This demo](https://github.com/fc7/volsync-demo/blob/main/pacman-gitops-volsync-restic) assumes the use of the External Secret Operator: we need to fine-tune it for our use cases.

2. TODO: integration to the Validated Pattern yaml?

## GCP

* Blank Open Environment is not suitable "out-of-the-box" for deploying OCP with RHACM
  --> many APIs need to be enabled and specific permissions need to be granted to the service account

*   