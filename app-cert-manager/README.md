# cert-manager
Managing TLS inside Kubernetes cluster is quite handy as you don't have to manage them at the host level e.g., installing web server (Nginx, Apache) and Certbot (etc).

## What this example do?
Configure a [cert-manager](https://cert-manager.io/docs/) to manage (request & auto-renewal) of Let's Encrypt certificates.

## Given
Assuming that I already added a [A Record](https://en.wikipedia.org/wiki/List_of_DNS_record_types) to my domain name registrar:

```
Type: A
Target: certmgr.sareno.dev
Value: 111.222.333.444
TTL: 300
```

## Requirements
- Kubernetes Cluster: [K3s](https://k3s.io/)
- Ingress Controller: `traefik`
- Domain name: `certmgr.sareno.dev`
- ACME Challenge Type: `HTTP`

## Run
```shell
$ kubectl apply -f acme-issuer.yaml
$ kubectl apply -f cert.yaml ### then wait for the certificate to be issued; arround ~5mins
$ kubectl apply -f nginx.yaml
```

Test it (from any machine):
```shell
$ curl https://certmgr.sareno.dev
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```

## References
- https://docs.k3s.io/quick-start
- https://cert-manager.io/docs/
