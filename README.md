# cloudrun-example-infra

This is a repository that contains the code used to set up the infra for the 
blog post [Deploying a Flask API to Google Cloud Run using Terraform](https://fpgmaas.com/blog/deploying-a-flask-api-to-cloudrun).

Pre-requisites to run:

- A GCP Project with a service account that has the following roles:

```
- Artifact Registry Administrator
- Cloud Run Admin
- Editor
- Project IAM Admin
- Service Usage Admin
```

## How to run?

- Download the Service Account Key in the `.json`-format, and place it in this repository.
- Run `cp .env.template .env` and set `GOOGLE_APPLICATION_CREDENTIALS` to the path to your service account file.
- Run `terraform init`
- Run `terraform validate`
- Run `source .env && terraform apply`