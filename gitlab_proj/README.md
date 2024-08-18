# Readme file for GitLab project

## Developing a Pyhton Web App using Flask

### Gitlab

- Has a image registry and the following uri can be found in the $CI_REGISTRY_IMAGE

- `registry.gitlab.com/[user_name]/[project_name]`
    - `/[image_name]:[tags]`

- image name can have up to three levels
    - `/[image_name]/[image_name]:[tags]`
    - `/[image_name]/[image_name]/[image_name]:[tags]`

- An access token should be passed to access the registry and should have minimum access for read & write
    - `read_registry` for read (pull) access
    - `write_redistry` for write (push) access

### Procfile

- Procfile is used declare the process types to specifies the commands that are executed by the app on start up included in the Heroku Apps.