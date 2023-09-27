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
 helm install kthamel-nginx bitnami/nginx --namespace=kthamel-dev <-- Do kubernetes deployment into the specific namespace
 helm list --namespace=kthamel-dev <-- List deployments, deployed from helm charts on specific namespace
 helm uninstall kthamel-nginx --namespace=kthamel-dev <--Do uninstall kubernetes deployment from the specific namespace
 helm upgrade nginx bitnami/nginx <-- Upgrade the version of helm deployment
 helm uninstall nginx --keep-history <-- Uninstall deployment and keep the track [kubectl get secrets]
helm install nginx bitnami/nginx --dry-run <-- Dry run execution syntax of Helm
helm template nginx bitnami/nginx > kthamel-nginx-pod-template.yam <-- Generate the helm template
helm get notes nginx <-- Get release notes of exixting deployment
helm get values nginx --all <-- Get all values of a existing deployment
helm get manifest nginx <-- Get the manifest that was used for the deployment
helm history nginx < Get the release history of a deployment 
helm rollback nginx <-- Rollback the existing version to the pervious version
helm install nginx bitnami/nginx --namespace=new --create-namespace <-- Deploying with creating new namespace
helm upgrade --install nginx bitnami/nginx <-- If not existing create deployment, if existing upgrade the version
helm install bitnami/nginx --generate-name --name-template "kthamel-{{randAlpha 5 | lower}}" <-- Generate name for deployment
helm install knginx-3 bitnami/nginx --wait <-- Wait till the pods up and running
helm install knginx-3 bitnami/nginx --atomic <-- If pods didn't came running state, rollback to previous version
helm create demo-nginx <-- Generate helm template according to the Nginx configuration
