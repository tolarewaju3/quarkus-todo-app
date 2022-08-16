# TODO Applications with Quarkus

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/cescoffier/quarkus-todo-app/Build)


## Starting the Application Locally

```bash
mvn quarkus:dev
```

Open: http://localhost:8080/

## Deploying to Kubernetes

Using Maven:

```bash
mvn clean package \
-Dquarkus.kubernetes.deploy=true \
-Dquarkus.container-image.builder=jib \
-Dquarkus.kubernetes-client.trust-certs=true
```

Using the CLI:

```bash
quarkus build \
-Dquarkus.kubernetes.deploy=true \ 
-Dquarkus.container-image.builder=jib \
-Dquarkus.kubernetes-client.trust-certs=true
```

## Deploying to OpenShift

Using Maven:

```bash
mvn clean package \
-Dquarkus.openshift.route.expose=true \
-Dquarkus.kubernetes.deploy=true \
-Dquarkus.container-image.builder=openshift \
-Dquarkus.kubernetes-client.trust-certs=true
```

Using Quarkus CLI:

```bash
quarkus build \
-Dquarkus.openshift.route.expose=true \
-Dquarkus.kubernetes.deploy=true \ 
-Dquarkus.container-image.builder=openshift \
-Dquarkus.kubernetes-client.trust-certs=true
```






