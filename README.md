# charts

Helm charts

https://github.com/helm/helm/blob/master/docs/chart_repository.md

## How this repo works

This repository has been configured in github to serve the `docs` folder.

Package each chart from the release tag of an upstream repository:

    helm package entity-service
    
    mv entity-service-x.y.z.tgz docs

Update the index:

    helm repo index docs --url https://n1analytics.github.io/charts
    
The commit and push.

For users:

    helm repo add n1 https://n1analytics.github.io/charts
    
    helm repo update
    
    helm install n1/entity-service [--values...]

