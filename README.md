init
# Flask Docker image

Flask Docker image powered by Python 3.5.1, with nginx and gunicorn. It is
aimed at a production use.

# Project quickstart

## Setup

1. Create a Dockerfile in the root of your project, starting with : `FROM yuxio/flask-python351`
2. Create a `requirements.txt` file containing your dependencies.

Note: you must have a file called `app.py` at the root of your project
with an `app` variable containing the Flask object.

## Running the project

```
docker build -t myapp .
docker run -d -P myapp
```

When you want to run the project (or update it), you just have to re-do these
two steps.

# General notes

- don't forget to check out the `sample-app` folder!
- everything in the folder `static` is served by nginx.
