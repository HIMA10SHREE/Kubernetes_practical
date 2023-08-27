
# Kubernetes basics:

to start kubernetes:
```bash
  minikube start
```

to check status of  kubernetes:
```bash
  minikube status
```

to check nodes:
```bash
 kubectl  get nodes
```

to create pod we write the pod.yml file: 
```bash
  apiVersion: v1
  kind: Pod
  metadata:
    name: nginx
  spec:
    containers:
    - name: nginx
      image: nginx:1.14.2
      ports:
      - containerPort: 80

```

to create pod:
```bash
  kubectl create –f pod.yml
```
to check pods
```bash
  kubectl get pods
```

to check complete pods details
```bash
  kubectl get pods -o wide
```

to delete pod
```bash
  kubectl delete pod nginx
```

To implement autohealing features:
```bash
  deployment-->replica set--->pod
```
![Screenshot (43)](https://github.com/HIMA10SHREE/Kubernetes_practical/assets/52618743/b0860b9c-1c4a-49ac-b2f5-9e8b9af9721f)

the replica set always creates the pod even when the pods get deleted.


to get sample yaml code:


![Screenshot (124)](https://github.com/HIMA10SHREE/Kubernetes_practical/assets/52618743/5e5e4cac-95db-4122-b7dc-e44b847e123f)
