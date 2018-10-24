## Accessing Data with MongoDB

Example to connect in a MongoDB Server with [Spring Boot](https://spring.io/guides/gs/accessing-data-mongodb/)

Using [Docker](https://hub.docker.com/_/mongo/).

**Setup**
```
# Use the oficial container
docker pull mongo
```

**Run mongodb server**
```
$ docker run --name mymongo -v [local-path]:/data/db -p 27017:27017 -d mongo

```

**Stop mongodb server**
```
$ docker stop mymongo
```

**Run**
```
$ mvn clean && mvn install
$ java -jar target/accessing-data-mongodb-0.0.1.jar 
```

**Test**
```
$ mongo 
 > show dbs
 > use test
 > show collections
 > db.customer.find()
```


