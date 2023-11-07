
# Example Django project with devcontainers

Check out the accompanying blog post here: https://backendclub.com/articles/django-dev-environment-vscode-remote-containers/

## Troubleshooting

You may encounter trouble getting the extension to forward ports automatically. This is most likely due to the Docker Compose file in the root folder of the project specifying ports. 

As described in my blog post, you may want to bind to `0.0.0.0:8000` by running `python manage.py runserver 0.0.0.0:8000`.

Alternatively, you could either:

- Remove ports from the `docker-compose.yml` file, OR
- Configure the extnesion to use a separate `docker-compose.yml` file.

For an example of how to do the second option, you can checkout the `separate-docker-compose-file` branch:

```
$ git checkout separate-docker-compose-file
```
