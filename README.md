# Helm Charts

Index of Data61 Helm charts.

See [chart repository documentation](https://github.com/helm/helm/blob/master/docs/chart_repository.md).

## To install a chart from this repository


    helm repo add data61 https://data61.github.io/charts
    
    helm repo update
    
    helm install data61/entity-service [--values...]



## How this repo works

This repository has been configured in github to serve the `docs` folder.

Package each chart from the release tag of an upstream repository:

    helm package entity-service
    mv entity-service-x.y.z.tgz docs

Update the index:

    helm repo index docs --url https://data61.github.io/charts
    
The commit and push.

