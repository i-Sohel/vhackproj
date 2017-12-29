# CI/CD plan for vanhack forum project

Using continuous integration & continuous delivery methods, we will deploy the vanhack forum app on [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine/).

## Deployment considerations
- [Kubernetes](https://kubernetes.io/) allowed us to deploy a highly available & scalable Java solution by using [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine/) as our solution platform.
- [Codefresh.io](https://codefresh.io) offers a complete CI/CD deployment pipeline on Kubernetes with a deep integration with Google Kubernetes Engine.
- [Maven](https://maven.apache.org/) is the main packaging solution to build the WAR file.
- [Tomcat](https://tomcat.apache.org/) is the server used to deploy the appliaction WAR file.


## Deployment pipeline flow
1. Codefresh monitors the Github repo for any changes.
2. When the developer pushes a change to the repo Codefresh picks the change.
3. Codefresh clones the main repo then builds the Docker image.
4. Codefresh pushes the new image to the Docker registry.
5. Codefresh starts the deployment script that deploys the solution on Google Cloud.

![](https://lh6.googleusercontent.com/MVNAe4XNLG2jxXxgRuY16jx823E7Os1uZMGqPn1Su1RFq1w07_x35qCD-WgGaxV8e84mqOPej6Qodyo28hh3=w3360-h1754)