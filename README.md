# ELK-Stack
1.  Elasticsearch

```
kubectl create -f elasticsearchservice.yaml
```
```
kubectl apply -f elasticsearchstatefulset.yam
```

Verify Elasticsearch Deployment

```
kubectl port-forward es-cluster-0 9200:9200

curl http://localhost:9200/_cluster/health/?pretty

```

2. Kibana

```
kubectl apply -f kibanadeployment.yaml
```
```
kubectl apply -f kibanaservice.yaml
```

Verify Kibana Deployment

```
kubectl port-forward <kibana-pod-name> 5601:5601
```

3. Fluentd

```
kubectl apply -f clusterrole.yaml
```
```
kubectl apply -f fluentdserviceaccount.yaml
```
```
kubectl apply -f fluentdset.yaml
```

 For Verifying the fluentd  create a pod and check the logs in Kibana. 
