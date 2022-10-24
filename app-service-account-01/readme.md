# Service Account 01
1. Create a secret with the following value:
    1. FART_BOMB_LAUNCH_CODE=bG9yZW0K
1. Create a service account named `secret-reader`
1. Create a ClusterRole that have access to the secret in #1
1. Create a RoleBinding and bind `secret-reader` service account to the role cluster in #3
1. Create a pod named `pod-can-read` that assumes the `secret-reader` service account
1. Create a pod named `pod-cannot-read` that assumes the default service account
1. Read the secret value on `pod-can-read` by running the following:
    ```sh
    kubectl exec pod-can-read -- cat /opt/secrets/FART_BOMB_LAUNCH_CODE
    ```
    You should get a `lorem` value
1. Read the secret value on `pod-canot-read` by running the following:
    ```sh
    kubectl exec pod-cannot-read -- cat /opt/secrets/FART_BOMB_LAUNCH_CODE
    ```
    You should get an empty value