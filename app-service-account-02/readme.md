# Service Account 02
Create a web app that accepts GET request from `/` and return the current Pod's status. Get the Pod's status thru apiservcer

## Tips
1. [Optional] Create a ServiceAccount
1. Create a Role with sufficient permissions to read the pods information
1. Create a RoleBinding and bind the service account to the role
1. Let to Pod use the service account

## Reference
* [https://kubernetes.io/docs/tasks/run-application/access-api-from-pod/](https://kubernetes.io/docs/tasks/run-application/access-api-from-pod/)
* [https://kubernetes.io/docs/reference/access-authn-authz/rbac/](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
* [https://kubernetes.io/docs/reference/kubernetes-api/authorization-resources/role-binding-v1/](https://kubernetes.io/docs/reference/kubernetes-api/authorization-resources/role-binding-v1/)
* [https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/)