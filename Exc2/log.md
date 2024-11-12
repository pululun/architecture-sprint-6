```shell
kubectl describe deployment scaletestapp
```
```shell
Name:                   scaletestapp
Namespace:              default
CreationTimestamp:      Tue, 12 Nov 2024 20:35:13 +0300
Labels:                 app=scaletestapp
Annotations:            deployment.kubernetes.io/revision: 1
Selector:               app=scaletestapp
Replicas:               5 desired | 5 updated | 5 total | 5 available | 0 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:  app=scaletestapp
  Containers:
   scaletestapp-container:
    Image:      shestera/scaletestapp
    Port:       8080/TCP
    Host Port:  0/TCP
    Limits:
      memory:  30Mi
    Requests:
      memory:      10Mi
    Environment:   <none>
    Mounts:        <none>
  Volumes:         <none>
  Node-Selectors:  <none>
  Tolerations:     <none>
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Progressing    True    NewReplicaSetAvailable
  Available      True    MinimumReplicasAvailable
OldReplicaSets:  <none>
NewReplicaSet:   scaletestapp-5b5b686c5 (5/5 replicas created)
Events:
  Type    Reason             Age   From                   Message
  ----    ------             ----  ----                   -------
  Normal  ScalingReplicaSet  49m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 1
  Normal  ScalingReplicaSet  48m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 2 from 1
  Normal  ScalingReplicaSet  44m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 3 from 2
  Normal  ScalingReplicaSet  43m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 4 from 3
  Normal  ScalingReplicaSet  42m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 5 from 4
  Normal  ScalingReplicaSet  40m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 7 from 5
  Normal  ScalingReplicaSet  38m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 8 from 7
  Normal  ScalingReplicaSet  37m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 9 from 8
  Normal  ScalingReplicaSet  36m   deployment-controller  Scaled up replica set scaletestapp-5b5b686c5 to 10 from 9
  Normal  ScalingReplicaSet  7m4s  deployment-controller  Scaled down replica set scaletestapp-5b5b686c5 to 9 from 10
  Normal  ScalingReplicaSet  5m4s  deployment-controller  Scaled down replica set scaletestapp-5b5b686c5 to 7 from 9
  Normal  ScalingReplicaSet  3m3s  deployment-controller  Scaled down replica set scaletestapp-5b5b686c5 to 6 from 7
  Normal  ScalingReplicaSet  3s    deployment-controller  Scaled down replica set scaletestapp-5b5b686c5 to 5 from 6
  
```
```shell
minikube addons list
```
```shell
|-----------------------------|----------|--------------|--------------------------------|
|         ADDON NAME          | PROFILE  |    STATUS    |           MAINTAINER           |
|-----------------------------|----------|--------------|--------------------------------|
| ambassador                  | minikube | disabled     | 3rd party (Ambassador)         |
| auto-pause                  | minikube | disabled     | minikube                       |
| cloud-spanner               | minikube | disabled     | Google                         |
| csi-hostpath-driver         | minikube | disabled     | Kubernetes                     |
| dashboard                   | minikube | enabled ✅   | Kubernetes                     |
| default-storageclass        | minikube | enabled ✅   | Kubernetes                     |
| efk                         | minikube | disabled     | 3rd party (Elastic)            |
| freshpod                    | minikube | disabled     | Google                         |
| gcp-auth                    | minikube | disabled     | Google                         |
| gvisor                      | minikube | disabled     | minikube                       |
| headlamp                    | minikube | disabled     | 3rd party (kinvolk.io)         |
| helm-tiller                 | minikube | disabled     | 3rd party (Helm)               |
| inaccel                     | minikube | disabled     | 3rd party (InAccel             |
|                             |          |              | [info@inaccel.com])            |
| ingress                     | minikube | enabled ✅   | Kubernetes                     |
| ingress-dns                 | minikube | disabled     | minikube                       |
| inspektor-gadget            | minikube | disabled     | 3rd party                      |
|                             |          |              | (inspektor-gadget.io)          |
| istio                       | minikube | disabled     | 3rd party (Istio)              |
| istio-provisioner           | minikube | disabled     | 3rd party (Istio)              |
| kong                        | minikube | disabled     | 3rd party (Kong HQ)            |
| kubeflow                    | minikube | disabled     | 3rd party                      |
| kubevirt                    | minikube | disabled     | 3rd party (KubeVirt)           |
| logviewer                   | minikube | disabled     | 3rd party (unknown)            |
| metallb                     | minikube | disabled     | 3rd party (MetalLB)            |
| metrics-server              | minikube | enabled ✅   | Kubernetes                     |
| nvidia-device-plugin        | minikube | disabled     | 3rd party (NVIDIA)             |
| nvidia-driver-installer     | minikube | disabled     | 3rd party (Nvidia)             |
| nvidia-gpu-device-plugin    | minikube | disabled     | 3rd party (Nvidia)             |
| olm                         | minikube | disabled     | 3rd party (Operator Framework) |
| pod-security-policy         | minikube | disabled     | 3rd party (unknown)            |
| portainer                   | minikube | disabled     | 3rd party (Portainer.io)       |
| registry                    | minikube | disabled     | minikube                       |
| registry-aliases            | minikube | disabled     | 3rd party (unknown)            |
| registry-creds              | minikube | disabled     | 3rd party (UPMC Enterprises)   |
| storage-provisioner         | minikube | enabled ✅   | minikube                       |
| storage-provisioner-gluster | minikube | disabled     | 3rd party (Gluster)            |
| storage-provisioner-rancher | minikube | disabled     | 3rd party (Rancher)            |
| volumesnapshots             | minikube | disabled     | Kubernetes                     |
| yakd                        | minikube | disabled     | 3rd party (marcnuri.com)       |
|-----------------------------|----------|--------------|--------------------------------|

```
  
