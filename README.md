# sonar-scanner-go

This docker image adds golang v1.13 and sonar-scanner 4.2 on top of java:alpine image. It is useful for integrating SonarQube for golang projects. I personally use this image in a custom helm chart.

Example to run this image:

```bash
export PROJECT_ROOT=~/your/path/to/golang/project

docker run -it --rm -v $PROJECT_ROOT:/app --name test-sonar-scanner-go \
--env SONARQUBE_SERVER=http://localhost:9000 --env SONARQUBE_PROJECT_KEY=project-key \
--env SONARQUBE_LOGIN=<sonarqube-token> raducrisan/sonarscanner-go

```

For more information, see: [Go for Sonarqube](https://medium.com/red6-es/go-for-sonarqube-ffff5b74f33a)
