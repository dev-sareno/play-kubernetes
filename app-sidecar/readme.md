# Sidecar
A Pod with multiple containers

## Setup
Containers in a Pod:
1. Nginx that accepts traffic from localhost:80 and creates log at `/var/log/nginx/localhost/access.log`
1. Flask web application that accepts GET request at `/` and returns the content of Nginx's log file

## Dev
```sh
kubectl apply -f 01-definition.yaml
```

### [Optional]
If you're using minikube and having trouble accessing NodePorts, run the ff.
```sh
minikube service nginx-flask-svc --url
```
then use the generated URLs

## Endpoints
1. Nginx (web): [http://localhost:30100](http://localhost:30100)
1. Flask (file reader): [http://localhost:30101](http://localhost:30101)