# gitops-demo

Very basic setup for demonstrating GitOps via Flux & ArgoCD.

`app1-base` represents a kustomization base configuration for an application we want to deploy. The "argocd" and "flux" directories contain environment-specific kustomizations (overlays). I've only separated them into 'argocd' and 'flux' to keep the demos independent; the overlays themselves are functionally identical.

The overlays reference `app1-base` via a relative path. In practice, the base might live in a different git repo and be referenced via a specific tag.

`demo-infra` just contains some supporting things for the demo; specifically Namespace declarations and some ArgoCD resources (Projects & Applications) which can also be configured via Argo's UI.
