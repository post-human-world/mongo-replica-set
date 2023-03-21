# Build up Mongo replica set

This repository need you run a few commands to set up replica set and it uses *docker compose* to launch the replica set. The *docker compose* file will deploy 3 separate containers:

- mongo1
    - set as primary with priority 7
    - map container port `27017` to localhost `27021`
- mongo2
- mongo3

All container are using one internal network so that them can connect to each other. Also they use same *mongod.cfg* and enabled key file authentication.

# Usage

1. Build up all containers

```bash
docker compose up -d --build 
```

2. Run script in mongo1 terminal. The script will initialize replica configuration and create a root user. This script may cost 30 seconds, because it need to wait node to become primary

```bash
/config/init.sh
```

3. Access mongodb with url: `mongodb://tom-rs:jerry@localhost:27021/?directConnection=true&authMechanism=DEFAULT`

# Reference

- [Create a replica set in MongoDB with Docker Compose](https://blog.tericcabrel.com/mongodb-replica-set-docker-compose/)
- [Deploy Replica Set With Keyfile Authentication](https://www.mongodb.com/docs/manual/tutorial/deploy-replica-set-with-keyfile-access-control/)