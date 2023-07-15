# terraform
kubectl run nginx --image=nginx --dry-run -o yaml
kubectl run nginx --image=nginx --dry-run -o yaml > firstpod.yaml
vi firstpod.yaml
kubectl create -f firstpod.yaml


Note:
#kubectl run nginx --image=nginx --dry-run -o yaml 
W0715 04:47:06.843755   17705 helpers.go:692] --dry-run is deprecated and can be replaced with --dry-run=client.
apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: null
  labels:
    run: nginx
  name: nginx		
spec:
  containers:
  - image: nginx
    name: nginx
    resources: {}
  dnsPolicy: ClusterFirst
  restartPolicy: Always
status: {}
