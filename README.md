# Usage

```bash
kubectl create secret docker-registry regcred --docker-server=index.docker.io --docker-username=username --docker-password=passwd --docker-email=ambrosia@gmail.com
kubectl create configmap nginx-proxy --from-file=configmap/nginx.conf
kubectl expose deployment frontend-teste --type=LoadBalancer --port=80
```
