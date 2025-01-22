# Instructions

## Prerequisites

- Kubernetes cluster
- Helm installed
- Access to the local Docker registry

## Deployment

1. Package the Helm chart:
    ```sh
    helm package .
    ```

2. Deploy the Helm chart:
    ```sh
    helm install vault-app-chart ./vault-app-chart-1.0.0.tgz
    ```

3. Verify the deployment:
    ```sh
    kubectl get pods
    kubectl get services
    ```

4. Access the Go app:
    ```sh
    kubectl port-forward svc/go-app 8080:8080
    ```

