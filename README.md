# Writing CI/CD for deployment via GitHub Actions
  This project enhances the CI/CD pipeline for deploying a Dockerized To-Do application using GitHub Actions. The workflow automates Docker image builds and pushes to DockerHub, with secrets securely managed. It includes Matrix testing across multiple Python versions (3.8, 3.9) and OS types (Ubuntu, Windows). The workflow supports manual triggers, allowing selection of specific artifacts for deployment. Branch protection, mandatory status checks, and manual approval for staging ensure controlled deployments. Concurrency control prevents multiple simultaneous runs, canceling previous ones when a new workflow starts. 

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
