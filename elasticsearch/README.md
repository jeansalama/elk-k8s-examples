# Elasticsearch Helm deployment

See this minikube [deployment config](https://github.com/elastic/helm-charts/tree/main/elasticsearch/examples/minikube) for more details.

Note that this configuration should be used for test only and isn't recommended
for production.

## Requirements

In order to properly support the required persistent volume claims for the
Elasticsearch StatefulSet, the `default-storageclass` and `storage-provisioner`
minikube addons must be enabled.

```
minikube addons enable default-storageclass
minikube addons enable storage-provisioner
```

## Deployment

```sh
helm repo add elastic https://helm.elastic.co
helm install elasticsearch elastic/elasticsearch \
    -n logstash \
    -f elasticsearch/helm/values.yml
```
