# Usage

You need to create a secret for the docker registry and a configmap for the nginx proxy.

## Secret

```bash
kubectl create secret docker-registry regcred --docker-server=index.docker.io --docker-username=username --docker-password=passwd --docker-email=ambrosia@gmail.com
```

## Configmap

```bash
kubectl create configmap nginx-proxy --from-file=configmap/nginx.conf
```

## Deployment

```bash
kubectl create -f deployment/frontend-teste.yml
```

## Expose LB
```bash
kubectl expose deployment frontend-teste --type=LoadBalancer --port=80
```
