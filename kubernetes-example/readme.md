# Kubernetes Example

This example will use the latest `verdaccio` tag. If you want you set a different that, update the `deployment.yaml` file.

* Install Minikube

https://github.com/kubernetes/minikube

```bash
$> brew cask install minikube
```

* Run it

```bash
$> minikube start
```

* Deploy

```bash
$> kubectl create -f deployment.yaml
deployment "verdaccio-deployment" created
```

* Check whether the Deployment was successful

```bash
$> kubectl get deployments
NAME                   DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
verdaccio-deployment   1         1         1            1           19m
```

* Deploy the service

```bash
$> kubectl create -f service.yaml
```

* Check the Service

```bash
kubectl get services
NAME         CLUSTER-IP   EXTERNAL-IP   PORT(S)          AGE
kubernetes   10.0.0.1     <none>        443/TCP          11h
verdaccio    10.0.0.160   <pending>     4873:30061/TCP   20m
```

* Browse the service

```bash
http://192.168.99.100:30061/
```

You can see the Dashboard in action

```
http://192.168.99.100:30000/#!/service?namespace=default
```
