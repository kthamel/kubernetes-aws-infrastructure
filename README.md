# kubernetes-aws-infrastructure

helm repo add bitnami https://charts.bitnami.io/bitnami <-- Add helm Bitnami repos
helm repo add stable https://charts.helm.sh/stable <-- Add helm stable version repos
helm repo list <-- List added repos
helm install nginx bitnami/nginx <-- Install using pod
helm uninstall nginx <-- Uninstall helm 
helm repo update <-- Update the helm
helm search repo stable <-- List available repos under stable
helm search repo nginx <-- Search the required one from the added repositories
helm search repo nginx --versions <-- List all the versions of the charts
 helm install kthamel-nginx bitnami/nginx --namespace=kthamel-dev <-- Do kubernetes deployment into the specific namespace.
 helm list --namespace=kthamel-dev <-- List deployments, deployed from helm charts on specific namespace
 helm uninstall kthamel-nginx --namespace=kthamel-dev <--Do uninstall kubernetes deployment from the specific namespace.
 