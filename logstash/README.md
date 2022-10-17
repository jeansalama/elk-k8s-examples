# Logstash Helm deployments

Note that this configuration should be used for test only and isn't recommended
for production.

## Requirements

Install [`elasticsearch`]() and [`kibana`]() helm charts

## 1 Logstash to Elasticsearch

```sh
helm repo add elastic https://helm.elastic.co
helm install logstash elastic/logstash \
    -n logstash \
    -f logstash/1_logstash/helm/values.yml
```

## 2..N Logstashes to Elasticsearch
TODO

## 2..N Logstashes to 1 ingress router to Elasticsearch
TODO

## 1 Filebeat to 1..N Logstashes to Elasticsearch
TODO

## 1..M Logstashes to 1 LoadBalancer to 2..N Logstashes to Elasticsearch
TODO

## And with kafka ?
TODO