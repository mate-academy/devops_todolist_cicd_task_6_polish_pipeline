# Django ToDo list

This is a to-do list web application with the basic features of most web apps, such as accounts/login, API, and interactive UI. 
To complete this task, you will need:

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Explore

Follow these steps to get the application up and running on your local machine (requires Python 3.8 or higher due to compatibility with Django 4):


```
pip install -r requirements.txt
```

Create a database schema:

```
python manage.py migrate
```

And then start the server (default is <http://localhost:8000>):

```
python manage.py runserver
```

You can now browse the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## Task

Extend the project's GitHub Actions workflow by integrating Docker to build and push images to DockerHub. 
This CI/CD enhancement involves several key tasks:

1. Update your forked repository with your DockerHub username and password.
    a. Add corresponding secrets to the repository.
2. Update `DockerImageName` with the DockerHub image repository name.
3. Use Matrix to run unit tests on different Python versions (3.8, 3.9).
4. Use Matrix to run unit tests on different OS types: Ubuntu and Windows.
5. Add input variables:
    a. Input variable to choose which artifact from the matrix to deploy. (windows-3.8, ubuntu-3.9, etc).tr
6. Add branch protection to the main branch in your fork.
7. Add mandatory pull requests and Python CI job status checks for PRs.
8. Add Manual Approval for the STG environment.
9. Allow to run only one workflow per pull request.
10. New runs should cancel the previous runs.
11. Create a Pull Request with the changes.
12. Pull Requests description should also contain a reference to a workflow run with successful workflow execution.
    


