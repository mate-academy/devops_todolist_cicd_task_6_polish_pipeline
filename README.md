# Enhanced CI/CD Pipeline with GitHub Actions

# Project Overview:

This project demonstrates the existing GitHub Actions CI/CD workflow by integrating Docker image building and pushing to DockerHub. It also introduces advanced workflow features such as matrix testing, manual workflow triggers, environment-specific deployments, and branch protection policies.

# Tech Stack:

- Python (Django)
- Docker & DockerHub
- Helm
- Kubernetes (Azure Kubernetes Service)
- GitHub Actions (CI/CD)
- GitHub Actions Environments & Secrets
- GitHub protection policies

# What was done:

- Stored DockerHub credentials, and other sensitive data as GitHub Actions repository/environment secrets.
- Developed a main and reusable GitHub Actions workflow to deploy Helm charts to an Kubernetes (kind)

- Continuous Integration included:

  - Matrix Testing:
    - Runs unit tests across multiple Python versions: 3.8, 3.9
    - Runs tests on both Ubuntu and Windows runners

  - Docker CI:
    - Created a Docker image of the Django application using semantic versioning.
    - The image is built and tagged automatically via GitHub Actions

  - Manual Workflow Dispatch:
    - Supports manual triggering with input selection (e.g., windows-3.8, ubuntu-3.9)
    - Enables flexible artifact selection for deployment

- Continuous Deployment  included:

  - Handled via a reusable workflow (deployment-workflow.yml) and triggered automatically on push to main.

  - Manual Approval:
    - Staging deployments require human approval before proceeding

  - Concurrency Control:
    - Only one workflow per PR is allowed
    - Ongoing runs are canceled if a new one starts

  - Branch Protection:
    - main branch is protected
    - enforces status checks and mandatory pull requests

  - Performs Helm dry-run to catch release issues early.
  - Executes atomic helm upgrade --install to ensure safe deployment

  - Supports multiple environments:
    - development
    - staging (with custom values/stg.yaml)

- Helm Charts included:
  - todoapp/: Helm chart for the Django application
  - mysql/: Reused chart from a previous task for MySQL backend

# Link to the successful GitHub Actions run:
https://github.com/konstantinou77/devops_todolist_cicd_task_6_polish_pipeline/actions/runs/14909718736

