---
title: Getting Started with Helm
parent: Getting Started
nav_order: 2
---
# Getting Started with Helm

### 1. Available Charts 

The following charts are available: 

* [vpw-analyzer-chart](https://github.com/viadee/vPW/tree/master/vpw-backend-parent/deployment/helm/vpw-analyzer-chart) 
* [vpw-pipeline-chart](https://github.com/viadee/vPW/tree/master/vpw-backend-parent/deployment/helm/vpw-pipeline-chart)
* [vpw-frontend](https://github.com/viadee/vPW/blob/master/vpw-backend-parent/deployment/helm-umbrella/vpw-chart/values.yaml) - values of vpw-frontend can be found in vpw-chart. 
* [vpw-polling-client-chart](https://github.com/viadee/camunda-kafka-polling-client/tree/master/camunda-kafka-polling-client/deployment/helm/vpw-polling-client-chart)  
* [vpw-chart](https://github.com/viadee/vPW/tree/master/vpw-backend-parent/deployment/helm-umbrella/vpw-chart) 

It is recommended to install the *vpw-chart*, since as an umbrella chart it combines all vpw components (vpw-analyzer-chart, vpw-pipeline-chart, vpw-frontend-chart, vpw-polling-client) and therefore allows an easy deployment.

### 2. Usage

* [Helm](https://helm.sh) must be installed to use the charts. Please refer to
  Helm's [documentation](https://helm.sh/docs) to get started.

* Once Helm has been set up correctly, add the repo as follows:

  `helm repo add viadee https://viadee.github.io/charts`

* If you had already added this repo earlier, run `helm repo update` to retrieve
  the latest versions of the packages.  You can then run `helm search repo
  viadee` to see the charts.

* To install the <chart-name> chart:

  `helm install my-<chart-name> viadee/<chart-name>`

* To uninstall the chart:

  `helm delete my-<chart-name>`

### 3. Set your own values

It is possible, and in most environments necessary, that the set default values of the charts need to be customized to your Kubernetes environment. Please refer to the values.yaml for each chart, especially to the `environment.secret` and `environment.configMap` sections. 
