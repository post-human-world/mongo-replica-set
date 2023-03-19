# Workflow

1. modify *compose volume* mapping, it is using my window10 path
   1. all configs and scripts are put into */xxx/mongodb/config*
   2. keyfile is in */xxx/mongodb/config/keys/keyfile.txt*
2. docker-compose up
3. run */config/init.sh* in primary node

# Reference

- [Create a replica set in MongoDB with Docker Compose](https://blog.tericcabrel.com/mongodb-replica-set-docker-compose/)
- [Deploy Replica Set With Keyfile Authentication](https://www.mongodb.com/docs/manual/tutorial/deploy-replica-set-with-keyfile-access-control/)