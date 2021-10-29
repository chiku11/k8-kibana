# Deploy Elastic search
```
kubectl apply -f es-deploy.yaml 
kubectl apply -f es-service.yaml
```

# Deploy Kibana
```
kubectl apply -f kibana-deploy.yaml 
kubectl apply -f kibana-service.yaml 
```

# Deploy FluentD DaemonSet
```
kubectl apply -f fluentd-daemonset.yaml
```

# Doc
https://coralogix.com/blog/kubernetes-logging-with-elasticsearch-fluentd-and-kibana/