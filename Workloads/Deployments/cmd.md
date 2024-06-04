kubectl apply -f nginx-deployment.yml
kubectl apply -f nginx-deployment-rollout.yml
kubectl rollout status deployment nginx-deployment
kubectl rollout history deployment nginx-deployment
kubectl delete deployment nginx-deployment