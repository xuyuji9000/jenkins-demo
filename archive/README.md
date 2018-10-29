# Commands

1. initialize jenkins

    `docker run --name myjenkins -p 8080:8080 -p 50000:50000 -u root -v $(which docker):/usr/bin/docker -v $PWD:/var/jenkins_home -d -v /var/run/docker.sock:/var/run/docker.sock jenkins`
