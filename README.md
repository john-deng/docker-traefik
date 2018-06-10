# Hosting Traefik with Docker

Træfik is a modern HTTP reverse proxy and load balancer that makes deploying microservices easy. Træfik integrates with your existing infrastructure components (Docker, Swarm mode, Kubernetes, Marathon, Consul, Etcd, Rancher, Amazon ECS, ...) and configures itself automatically and dynamically. Pointing Træfik at your orchestrator should be the only configuration step you need.

## Getting started

Bring up Traefik site is really easy by using install All you have to do is clone the source and then run the script wordpress

### Clone the repo

```bash
git clone https://github.com/john-deng/docker-wordpress.git
```

### Change directory

```bash
cd docker-wordpress
```

### Type command ./install for the first time

```bash
./install
```

### or ./install -r if you want reset all settings

```bash
./install -r
```

wordpress will prompt below input requests, please input your site parameters or just type enter if your want to user the default settings

```bash

[INPUT] Domain [example.com]:
[INPUT] Email [your.name@example.com]:

Use example.com as your site domain? [yes/no] y

```

```bash
docker-compose up -d
```

wordpress show up and running ...

```bash

Creating dockerwordpress_db_1 ... done
Creating dockerwordpress_wordpress_1 ... done

```

### Show docker-compose status

```bash
docker-compose ps
```

here is the status

```bash
           Name                          Command               State           Ports
--------------------------------------------------------------------------------------------
dockerwordpress_db_1          docker-entrypoint.sh mysqld      Up      3306/tcp
dockerwordpress_wordpress_1   docker-entrypoint.sh apach ...   Up      0.0.0.0:32823->80/tcp

```

### Shutdown wordpress

If you want to shutdown wordpress, just type docker-compose down

```bash
docker-compose down
```

```bash
Stopping dockerwordpress_wordpress_1 ... done
Stopping dockerwordpress_db_1        ... done
Removing dockerwordpress_wordpress_1 ... done
Removing dockerwordpress_db_1        ... done
Network web is external, skipping

```