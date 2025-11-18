Helm packaging of the CTF web application

## Prerequisites

Make sure [cert-manager](https://cert-manager.io) is installed in the cluster before deploying the application.

## Deployment with Helmfile

First, clone the helm repository.

```bash
git clone https://github.com/ctflags/helm.git
cd helm
```

Next, create a `values.yaml` following the example of [this one](./values.yaml). 

Note: You need to provide a Postgres connection URL. This can be a local or a hosted one.

Next, verify the templates are correctly rendered.

```bash
helmfile templates
```

Then, deploy the application.

```bash
helmfile apply
```

## Deployment with the helm Cart

WIP: helm chart to be released soon (currently being moved to another registry).