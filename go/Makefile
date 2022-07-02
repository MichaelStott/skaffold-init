
DEPLOY_ENV ?= local

repo: ## Add required Helm chart repositories.
	helm repo add bitnami https://charts.bitnami.com/bitnami
	helm repo update

cluster: ## Provision a local k8s cluster for development.
	kind create cluster --name local-k8s

buster: ## Delete local cluster.
	kind delete cluster --name local-k8s

dev: ## Run application in dev mode.
	skaffold dev -p local -f deploy/skaffold/skaffold.yaml --port-forward

run: ## Deploy app to target cluster.
	skaffold run -f deploy/skaffold/skaffold.yaml
