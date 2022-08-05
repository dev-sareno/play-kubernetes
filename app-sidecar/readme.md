# Sidecar
A Pod with multiple containers

## Setup
Containers in a Pod:
1. Nginx that accepts traffic from localhost:80 and creates log at `/var/log/nginx/localhost.access.log`
1. Flask web application that accepts GET request at `/` and returns the content of Nginx's log file