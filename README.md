# kgateway-field-kit GitOps tree

This repo is the external GitOps target for [kgateway-field-kit](https://github.com/day0ops/kgateway-field-kit)'s
use-case library. `kgw usecase deploy <name>` renders a use case's resources to static YAML and
commits them into `usecases/<name>/` here; ArgoCD's `ApplicationSet` (bootstrapped by the `argocd`
addon) watches this directory and syncs each use case into its own namespace.
