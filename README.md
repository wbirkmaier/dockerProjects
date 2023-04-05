# dockerProjects

Simple project space for building docker stuff, you of course need docker installed:
```
brew install docker
```

$ docker build -t hello-world-app .
$ docker run -it --rm --name hello-world-running-app hello-world-app

-or-

$ docker run -d hello-world-app


or a single line:

$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp python:3 python your-daemon-or-script.py

examples:
docker run --name repo alpine/git clone https://github.com/docker/getting-started.git
docker cp repo:/git/getting-started/ .
cd getting-started
docker build -t docker101tutorial .
docker run -d -p 80:80 --name docker-tutorial docker101tutorial
