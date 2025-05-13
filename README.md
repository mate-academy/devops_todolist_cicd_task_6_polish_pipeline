# Django ToDo list

This is a to-do list web application with the basic features of most web apps, such as accounts/login, API, and interactive UI.

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Summary

- In this project, I enhanced the GitHub Actions CI/CD pipeline with matrix testing, manual deployment control, and security improvements:

- Added DockerHub credentials and updated the DockerImageName in the repository.

- Created environment secrets for development and staging environments.

- Used matrix strategy to run unit tests on:

    - Python versions: 3.8 and 3.9

    - Operating systems: ubuntu-latest and windows-latest

- Enabled manual workflow run with input variables to select which matrix artifact to deploy (e.g., ubuntu-3.9, windows-3.8).

- Enabled concurrency to allow only one active workflow per pull request - new runs cancel the previous ones.

- Configured branch protection on the main branch, requiring:

    - Mandatory pull requests

    - Successful Python CI checks

- Added manual approval step for deployments to the staging environment.
