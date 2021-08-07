# gitlab
This repository teach you how to build your own github-gitlab within container
#Prerequisite
You have installed docker and docker-compose
#Quikely start
1. Choose your gitlab 'HOME_DIR' and set the environment variable 'GITLAB_HOME', e.g.
'''bash
export GITLAB_HOME=$HOME/gitlab
'''
2. Download the *docker-compose.yml* file and move it to '$GITLAB_HOME' directory, Then execute 'docker-compose up'

3. Do not worry! It need a few minutes for the container to be healthy. You can use 'docker ps' to check the status of the container.

When the container is healthy, step in it and execute 'gitlab-rails console'
'''shell
docker exec <container's ID> -it /bin/bash
gitlab-rails console
u.password='qweqweqwe'
u.password_confirmation='qweqweqwe'
u.save
'''
Now, you can log in with root acount via <ip>:8939
