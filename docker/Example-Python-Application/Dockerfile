# We are using python as base image
FROM python:3

# Installing gunicorn flask
RUN pip install gunicorn flask

# Adding the Python Code to the Image
ADD mainapp.py wsgi.py /app/

# Exposing the port on which application will be exposed
EXPOSE 5000

# Changing the working directory of Container to be /app
WORKDIR /app


ENTRYPOINT [ "gunicorn","--bind","0.0.0.0:5000","wsgi:app" ]
