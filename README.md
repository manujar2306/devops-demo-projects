***********Apply Resources************

kubectl apply -f ubuntu.yaml
kubectl apply -f nginx.yaml
kubectl apply -f multi-container.yaml

***********Verify Pods**************
kubectl get pods -o wide

************View Logs***************
kubectl logs ubuntu-pod
kubectl logs nginx-pod

kubectl logs multi-container-demo -c alpine-container
kubectl logs multi-container-demo -c tomcat-container

*************Describe pod (debugging)******************
kubectl describe pod multi-container-demo

*************Exec into container***********************
kubectl exec -it ubuntu-pod -- bash
kubectl exec -it multi-container-demo -c alpine-container -- sh

