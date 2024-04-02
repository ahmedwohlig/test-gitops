# Deployment.apps Module

This module is designed to create deployments using ArgoCD from YAML files.

## Prerequisites

Before using this module, make sure you have the following prerequisites installed:

- ArgoCD: [Installation Guide](https://argoproj.github.io/argo-cd/getting_started/)
- Kubernetes: [Installation Guide](https://kubernetes.io/docs/setup/)

## Usage

To use this module, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/deployment.apps.git
    ```

2. Navigate to the `deployment.apps` directory:

    ```bash
    cd deployment.apps
    ```

3. Create your deployment YAML files in the `manifests` directory.

4. Deploy the YAML files using ArgoCD:

    ```bash
    argocd app create my-app --repo https://github.com/your-username/deployment.apps.git --path manifests --dest-server https://kubernetes.default.svc --dest-namespace my-namespace
    ```

    Replace `my-app`, `your-username`, `my-namespace` with your desired values.

5. Verify that the deployments are created successfully:

    ```bash
    kubectl get deployments -n my-namespace
    ```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
