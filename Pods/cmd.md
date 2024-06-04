kubectl apply -f nginx-pod.yml
kubectl create -f nginx-pod.yml
kubectl get pods
kubectl describe pod my-nginx
kubectl delete pod my-nginx
kubectl port-forward my-nginx 8080:80
kubectl exec my-nginx -it -- bash
kubectl logs my-nginx # -c container-name
kubectl top my-nginx

