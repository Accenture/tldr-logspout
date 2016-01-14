# Introduction

Logspout.

# Building

```
docker build -t tldr/logspout .
```

# Running

```
docker run -d --name logspout -h logspout -p 8100:8000 -v /var/run/docker.sock:/tmp/docker.sock tldr/logspout syslog://$(docker-machine ip tldr-dev):5000
```