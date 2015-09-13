## GoCD Agent + Docker in a Docker + JRuby
In a container!

We needed JRuby in some of our deployments, and therefore we created this container. Uses `tispr/gocd-agent-dind` as a base image. Adds **JRE** and **JRuby 9.0.1.0**

**Usage**

```
docker pull foundry/gocd-dind-jruby
```

To start this as a daemon, run the following:

```
docker run -d --privileged foundry/gocd-dind-jruby
```

*--privileged* = required in order to run docker inside the box (without privileged, you will be unable to run docker commands e.g. `docker images`).

