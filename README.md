<h1 align="">DevOps exam deploy on k8s 👋</h1>
<p>
</p>

> DevOps exam deploy on k8s

![k8s](/.github/assets/img/kubernetes-logo.png)

## Table of Contents

* **Kubernetes**
  * [Official Website](https://kubernetes.io)
  * [Official Docs](https://kubernetes.io/docs/home/)
  * [Official Github](https://github.com/kubernetes)

## Requirements
* kubernetes cluster + kubectl;

## Usage

```
kubectl create secret docker-registry regcred --docker-server=index.docker.io --docker-username=username --docker-password=passwd --docker-email=ambrosia@gmail.com
kubectl create configmap nginx-proxy --from-file=configmap/nginx.conf
kubectl create -f deployment/frontend-teste.yml
kubectl expose deployment frontend-teste --type=LoadBalancer --port=80
```
# References
https://docs.gitlab.com/ee/user/project/clusters/add_remove_clusters.html
https://about.gitlab.com/handbook/customer-success/demo-systems/tutorials/getting-started/configuring-group-cluster  
https://medium.com/@yanick.witschi/automated-kubernetes-deployments-with-gitlab-helm-and-traefik-4e54bec47dcf

## Author

👤 **Tadeu Bernacchi**

* Website: http://www.tadeubernacchi.com.br/
* Twitter: [@tadeuuuuu](https://twitter.com/tadeuuuuu)
* Github: [@tbernacchi](https://github.com/tbernacchi)
* LinkedIn: [@tadeubernacchi](https://linkedin.com/in/tadeubernacchi)

## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
