# charts

Helm charts


## How this repo works

This repository has been configured in github to serve the `docs` folder.

Package each chart from the release tag of an upstream repository:

    helm package linkage-service
    
    mv linkage-service-x.y.z.tgz docs

    helm repo index docs --url https://n1analytics.github.com/charts
    

For users:

    helm repo add n1charts https://n1analytics.github.com/charts

