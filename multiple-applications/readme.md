# Multiple Applications
Create a cluster that consists multiple projects/apps.

### Note
Each variety must have its own namespace

### Namespaces

### Product
1. Creates 2 namespaces `company-abc` and `company-xyz`
1. Runs Nginx deployment with 1 replica on `company-abc` namespace. Access here [http://localhost:30100/](http://localhost:30100/)
1. Runs whoami deployment with 3 replicas on `company-xyz` namespace. Access here [http://localhost:30101/](http://localhost:30101/)

### Run
```sh
kubectl apply -f .
```
