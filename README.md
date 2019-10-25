# simple-python-pyinstaller-app

This repository is for the
[Build a Python app with PyInstaller](https://jenkins.io/doc/tutorials/build-a-python-app-with-pyinstaller/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

The repository contains a simple Python application which is a command line tool "add2vals" that outputs the addition of two values. If at least one of the
values is a string, "add2vals" treats both values as a string and instead
concatenates the values. The "add2" function in the "calc" library (which
"add2vals" imports) is accompanied by a set of unit tests. These are tested with pytest to check that this function works as expected and the results are saved
to a JUnit XML report.

The delivery of the "add2vals" tool through PyInstaller converts this tool into
a standalone executable file for Linux, which you can download through Jenkins
and execute at the command line on Linux machines without Python.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial.


## Jenkins container

```
docker run \
  --rm \
  -u root \
  -p 8080:8080 \
  -v jenkins-data:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v "$HOME":/home \
  jenkinsci/blueocean
```

```
docker exec -it  e9e4b1fb9d05 bash
```

```
printenv
```

```
bash-4.4# printenv
JENKINS_SLAVE_AGENT_PORT=50000
LANG=C.UTF-8
HOSTNAME=e9e4b1fb9d05
JENKINS_UC=https://updates.jenkins.io
JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
JAVA_VERSION=8u212
PWD=/root
HOME=/root
COPY_REFERENCE_FILE_LOG=/var/jenkins_home/copy_reference_file.log
JENKINS_HOME=/var/jenkins_home
REF=/usr/share/jenkins/ref
TERM=xterm
JENKINS_INCREMENTALS_REPO_MIRROR=https://repo.jenkins-ci.org/incrementals
SHLVL=1
JENKINS_UC_EXPERIMENTAL=https://updates.jenkins.io/experimental
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
JAVA_ALPINE_VERSION=8.212.04-r0
JENKINS_VERSION=2.190.1
_=/bin/printenv
OLDPWD=/
```


