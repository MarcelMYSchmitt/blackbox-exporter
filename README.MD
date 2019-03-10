# Blackbox Exporter
Is used to periodically call other services and transform the result into Prometheus format.
More information: https://github.com/prometheus/blackbox_exporter

## Prerequisites
Please make sure to adjust the values in the specific helm deployment value files. 

## Deployment
```
helm --kube-context dev --namespace 'namespacename' upgrade 'helminstallname' ./Blackbox/deployment/ --install --recreate-pods
```

# Prometheus
Configured to scrape the blackbox.

## Prerequisites
Please make sure to adjust the values in the specific helm deployment value files. 

## Deployment
```
helm --kube-context dev --namespace 'namespacename' upgrade 'helminstallname' ./Prometheus/deployment/ --install --recreate-pods
```