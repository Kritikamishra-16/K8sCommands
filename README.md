# K8s Commands

## To list namespaces
```
kubectl get ns 
kubectl get namespace
```

## To create new namespace
```
kubectl create ns <namespace_name>
kubectl create jiorooms
```

## To list pods/ services/ configmaps/ replicaset
```
kubectl get pods -n <namespace_name>
kubectl get services -n <namespace_name>  OR kubectl get svc -n <namespace_name> 
kubectl configmap -n <namespace_name>  OR kubectl cm -n <namespace_name>
kubectl serviceaccount -n <namespace_name> OR kubectl sa -n <namespace_name>
kubectl secrets -n <namespace_name> 
kubectl rs -n <namespace_name>
```

## To create configMap
```
kubectl create configmap <configmap_name> --from-file=<config_folder/config_file>/ -n <namespace_name>
kubectl create configmap jioroom-config --from-file=jioroom-config/ -n jiorooms
```

## To apply deployments/ Services
```
Go inside the deployments folder in which the server.yaml files are present
kubectl apply -f api-server.yaml

Go inside the services folder in which the api-server-svc.yaml files are present
kubectl apply -f api-server-svc.yaml

```

## To get all deployments status
```
kubectl get deployments -A
kubectl get deployments -n <namespace_name>
```

## Describe deployments/ replica set 
```
To get detailed information about  service deployment
kubectl describe sa <service_name> -n <namespace_name>
kubectl describe deployments <deployment_name> -n <namespace_name>
kubectl describe rs <replica_set_name> -n <namespace_name>
```

## To delete deployments
```
kubectl delete deployments <deployment_name> -n <namespace_name>
kubectl delete pods <pod_name> -n <namespace_name>
kubectl delete svc <service_name> -n <namespace_name>
kubectl delete cm <config_map_name> -n <namespace_name>
```
## To see logs of a pod
```
kubectl logs -f <pod_name> -n <namespace_name>
```

## To exec in pod
```
kubectl exec -it <pod_name> -n <namespace_name> -- bash
```



















