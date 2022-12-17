# Custom Jenkins integration running in a DOcker Container with Docker tools installed

Steps:

1. Build the custom Jenkins image from the DOckerfile in ./CustomJenkinsWithDocker
```
docker image build -t custom-jenkins-docker .
```
2. Run a Jenkins instance with Docker. You need to pass the Docker daemon socket in a volume
```
$ docker run -it -p 8080:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock -v jenkins_home:/var/jenkins_home custom-jenkins-docker
```


// Also see https://hackmamba.io/blog/2022/04/running-docker-in-a-jenkins-container/