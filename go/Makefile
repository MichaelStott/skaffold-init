
DEPLOY_ENV?=local

cluster: ## Provision a local k8s cluster for development.
	kind create cluster --name kind-local

buster: ## Provision a local k8s cluster for development.
	kind delete cluster --name kind-local

dev: ## Run application in dev mode.
	skaffold dev -f skaffold/skaffold.yaml --port-forward

deploy: ## Deploy app to target cluster.
	skaffold run -f skaffold/skaffold.yaml
