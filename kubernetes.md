
# Kubernetes basics:

to start kubernetes:
```bash
  minikube start
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


