# Hosting Traefik with Docker

Træfik is a modern HTTP reverse proxy and load balancer that makes deploying microservices easy. Træfik integrates with your existing infrastructure components (Docker, Swarm mode, Kubernetes, Marathon, Consul, Etcd, Rancher, Amazon ECS, ...) and configures itself automatically and dynamically. Pointing Træfik at your orchestrator should be the only configuration step you need.

## Getting started

Bring up Traefik site is really easy by using install All you have to do is clone the source and then run the script traefik

### Clone the repo

```bash
git clone https://github.com/john-deng/docker-traefik.git
```

### Change directory

```bash
cd docker-traefik
```

### Type command ./install for the first time

```bash
./install
```

### or ./install -r if you want reset all settings

```bash
./install -r
```

traefik will prompt below input requests, please input your site parameters or just type enter if your want to user the default settings

```bash

[INPUT] Domain [example.com]:
[INPUT] Email [your.name@example.com]:

Use example.com as your site domain? [yes/no] y

Done

```

After traefik is installed, then run docker-compose

```bash
docker-compose up -d
```

traefik show up and running ...
