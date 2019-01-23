# Hello-World

Execute below steps to deploy pods.

  - Deploy pods
  ```sh
  kubectl apply -f hello.yaml
  kubectl get deployments
  kubectl get pods --output=wide
  ```
  - Note the Nodeport number 
  ```sh
  kubectl describe services hello-k8s-service
  ```
  - Expose deployment to outside world
  ```sh
  kubectl expose deployment hello-k8s-deployment
  ```
  - Find out pulic ip of master node
  ```sh
  kubectl cluster-info
  ```
  or execute below command which will display <ip-address>:<port>
  ```sh
  minikube service hello-k8s-service --url=true
  ```
  ex :- 
  ```sh
  C:\Users\mcmanjun>minikube service hello-k8s-service --url=true
  http://192.168.99.103:32250
  ```
  - Access your service via browser or curl
    http://<<ip-of-vm>>:32250

