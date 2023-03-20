# Workflow

1. docker-compose up
2. run `/config/init.sh` in mongo1 terminal
3. Access mongodb with url: `mongodb://tom-rs:jerry@localhost:27021/?directConnection=true&authMechanism=DEFAULT`

# Reference

- [Create a replica set in MongoDB with Docker Compose](https://blog.tericcabrel.com/mongodb-replica-set-docker-compose/)
- [Deploy Replica Set With Keyfile Authentication](https://www.mongodb.com/docs/manual/tutorial/deploy-replica-set-with-keyfile-access-control/)