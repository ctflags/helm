Helm packaging of the CTF web application

## Prerequisites

Make sure [cert-manager](https://cert-manager.io) is installed in the cluster before deploying the application.

## Deployment with Helmfile

First, clone the helm repository.

```bash
git clone https://github.com/ctflags/helm.git
cd helm
```

Next, modify `values.yaml`:

- you can provide a Postgres connection string with `database.url`. if not provided, a local Postgres database will be run.
- under `config`, update the `challenges`, `participants` and `organizers` properties.

Next, verify the templates are correctly rendered.

```bash
helmfile templates
```

Then, deploy the application.

```bash
helmfile apply
```

## Removing the application

```bash
helmfile destroy
```