# My development environment

My development environment is a docker-compose project that has the following elements:

- Sonarqube
- Artifactory
- Jenkins

You must create an environment variable called VOLUMES_PATH in which we must set the path for the volumes to be used by the containers.

- docker-compose up: To start the containers
- docker-compose up -d: To start the containers in daemon mode
- docker-compose stop: To stop the containers
- docker-compose rm -f -v: To remove the containers and its volumes

## Sonarqube

Sonarqube is an open source platform for continuous inspection of code quality. We are using images from [the official Docker repository](https://hub.docker.com/_/sonarqube/).

We are also using a PostgreSQL database [the official Docker repository](https://hub.docker.com/_/postgres/).

- User: admin
- Password: admin

http://localhost:9000

## Artifactory

Artifactory is a software repository manager. We are using the open source version following the instructions from [its official web](https://www.jfrog.com/confluence/display/RTF/Running+Artifactory+OSS).

When it starts, the following default admin user is created:

- User: admin
- Password: password

http://localhost:8081

## Jenkins

Jenkins is a Continuous Integration and Delivery server. We are using images from [the official Docker repository](https://hub.docker.com/_/jenkins/).

When it starts the first time, an admin password is created.

http://localhost:8080
