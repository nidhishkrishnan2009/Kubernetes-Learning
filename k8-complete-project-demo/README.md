# this project contains 2 apps
1. Mongo DB
2. Mongo Express

# Components of Mongo DB:
1. pod
2. deployment
3. internal service [which means only components with in the cluster can talk]

# Components of Mongo Express
1. pod
2. deployment
3. external service
4. configMap [where db urls and other properties are stored]
5. Secrets [where DB username & passwords are stored]

configMap & Secrets will be referenced in deployment component

Architecture:

Browser ---> Mongo Express External svc ---> Mongo Express pod ---> Mongodb internal service -> Mongo DB pod

Steps:

1. Created mongodb-Secret
2. Created mongodb-Deployment
3. Created mongodb-internal-service
4. Created MongoExpress-ConfigMap
5. Created MongoExpress-deployment
6. Created MongoExpress-External-Service
