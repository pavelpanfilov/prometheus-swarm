# prometheus-swarm
Prometheus for docker swarm cluster with common exporters

Set variables starting with YOUR-*

Update target nodes with monitoring label:
```shell
$ docker node update --label-add monitoring=true YOUR_NODE
```

Deploy stack with timestamped configs:
```shell
$ ADMIN_PASSWORD="YOUR_PASSWORD" ADMIN_USER="YOUR_USER" TIMESTAMP="mon_$(date +%d.%m.%Y-%H%M%S)" docker stack deploy -c docker-compose.yml mon
```