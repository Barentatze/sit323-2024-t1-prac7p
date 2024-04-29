# Jifeng Chen's 6.1P: Creating a Kubernetes Cluster for a containerized application

This is the Jifeng Chen's implementation of SIT323 6.1P

To utilize this demonstration, please follow the steps below:

1. **Firstly**, creating a k8s dashboard and get the token:
    ```bash
    kubectl apply -f ./create-dashboard-ui.yaml
    kubectl apply -f ./dashboard-adminuser.yaml
    kubectl -n kubernetes-dashboard create token admin-user
    ```
   You need to use the following command to start a dashboard:
   ```bash
   kubectl proxy
   ```

2. **Next**, create the k8s pods and replicas using the following commands:
    ```bash
    kubectl apply -f ./createPods.yaml
    kubectl apply -f ./createReplicaSet.yaml
    ```
3. **Then**, create the k8s service using the following commands:
    ```bash
    kubectl apply -f ./createService.yaml
    ```
4. **Finally**, test the following websites to check the execution of both two services
    http://localhost:8037/exponentiation?n1=10&n2=6 <br>
    http://localhost:8037/exponentiation?n1=10&n2=6

