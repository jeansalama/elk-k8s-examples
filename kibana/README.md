# Kibana Helm deployment

Note that this configuration should be used for test only and isn't recommended
for production.


## Deployment

```sh
helm repo add elastic https://helm.elastic.co
helm install kibana elastic/kibana \
    -n logstash \
    -f kibana/helm/values.yml
```
