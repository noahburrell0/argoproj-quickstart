## Getting Started

This assumes that you already have an Argo CD instance running, and a cluster added that you wish to deploy the argoproj components into.

1. Fork repository
1. Find and replace all instances of `noahburrell0` with your username/organization
1. Create a new app in Argo CD
    1. Click the "+ NEW APP" button
    1. Click the "EDIT AS YAML"
    1. Copy and paste the contents of `app-of-apps.yaml`
    1. Click "SAVE"
    1. Click "CREATE"
1. Label the cluster/s you wish to deploy to with `argoproj-components: "true"`
1. Argoproj components (Rollouts, Workflows, and Events) will automatically be synced to the labeled clusters.
1. Example apps for Rollouts and Workflows can be manually synced

To view the Argo Workflows UI locally run the following:
kubectl -n argo port-forward service/argo-server 2746:2746
