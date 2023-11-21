# Kube-Operator

以下をもとにKube-Operatorを起動



https://github.com/cdsl-research/Kube-Operator


# Kube-Collectorの使い方

Kube-CollectorとはKube-Operatorのための監視エージェントです

Kube-Operatorと併用して使います．

## 使い方
step1

```
$ kubectl create namespace python
```

step2

```
$ cd Kube-Collector/Collector/
```

step3

```
$ kubectl apply -k . -n python
configmap/myapp-8gkg849b9g created
service/agent-service created
deployment.apps/agent created
```

step4
```
$ kubectl get pods -n python -w
NAME                     READY   STATUS              RESTARTS   AGE
agent-7fcd655cb8-rzmh7   0/1     ContainerCreating   0          7s
agent-7fcd655cb8-rzmh7   1/1     Running             0          16s
```


