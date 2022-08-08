# Service Account 02
Create a web app that accepts GET request from `/` and return the API Server `/api/v1/` content.

## Tips
1. [Optional] Create a ServiceAccount
1. Create a ClusterRole with sufficient permissions to read the pods information
1. Create a RoleBinding and bind the service account to the cluster role
1. Attach the service account to the pod

## Reference
* [https://kubernetes.io/docs/tasks/run-application/access-api-from-pod/](https://kubernetes.io/docs/tasks/run-application/access-api-from-pod/)
* [https://kubernetes.io/docs/reference/access-authn-authz/rbac/](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
* [https://kubernetes.io/docs/reference/kubernetes-api/authorization-resources/role-binding-v1/](https://kubernetes.io/docs/reference/kubernetes-api/authorization-resources/role-binding-v1/)
* [https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/)