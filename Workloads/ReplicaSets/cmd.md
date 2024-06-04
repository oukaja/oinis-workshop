Kubectl apply -f nginx-replicaset.yml
Kubectl scale rs nginx-rs --replicas=3
kubectl delete replicaset nginx-rs
kubectl delete replicaset nginx-rs --cascade=orphan