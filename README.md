# Github Actions for ECR Build & ECS Fargate Release

### Environment
This action uses environment authorization for the AWS CLI.
```
env:
  AWS_ACCESS_KEY_ID: ${{ secrets.YOUR_AWS_ACCESS_KEY_ID }}
  AWS_SECRET_ACCESS_KEY: ${{ secrets.YOUR_AWS_SECRET_ACCESS_KEY }}
  AWS_REGION: us-east-1
```

### Inputs
```
inputs:
  ecr-repo:
    description: The ECR Repo name without the ECR Registry portion.
    required: true
  app-env:
    description: The APP_ENV (use action-build-vars.appEnv)
    required: true
  release:
    description: The release tag (action-build-vars.release)
    required: true
  task-definition:
    description: The path to the task definiton
    required: true
  task-container:
    description: The container within the task to use
    default: web-container
    required: false
  service:
    description: The ECS/Fargate Service name
    required: true
```