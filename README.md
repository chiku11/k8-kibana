# Deploy Elastic search
kubectl apply -f es-deploy.yaml 
kubectl apply -f es-service.yaml 

# Deploy Kibana
kubectl apply -f kibana-deploy.yaml 
kubectl apply -f kibana-service.yaml 


# Deploy Logstash
kubectl create configmap logstash-pipeline --from-file ./logstash.conf
kubectl apply -f logstash-deploy.yaml 
kubectl apply -f logstash-service.yaml

#Deploy Filebeat
kubectl create configmap filebeat-pipeline --from-file ./filebeat.conf
kubectl apply -f filebeat-deploy.yaml

##
Refer: https://coralogix.com/blog/elasticsearch-logstash-kibana-on-kubernetes/