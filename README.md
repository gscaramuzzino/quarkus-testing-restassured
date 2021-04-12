# Test a Quarkus application with REST Assured and H2 Database

Simple project that shows you how to test a Quarkus application with REST Assured and H2 Database.

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/.

## Follow the video tutorial:

[![Alt text](https://user-images.githubusercontent.com/8536722/110162186-aa6eab00-7dee-11eb-8289-bd3cf6c13a11.png)](https://youtu.be/zs8aN5g0lr0 "Click to play on Youtube.com")

## Test the application
```shell script
mvn compile test
```


## Running the application in dev mode
```shell script
docker pull postgres
docker run --name my_db \ 
      -e POSTGRES_USER=username \
     -e POSTGRES_PASSWORD=password \
     -e POSTGRES_DB=my_db \
     -p 5432:5432 \
     postgres:10.5
```

You can run your application in dev mode that enables live coding using:
```shell script
mvn compile quarkus:dev
```

## Packaging and running the application

The application can be packaged using:
```shell script
mvn package
```
It produces the `quarkus-testing-restassured-1.0.0-SNAPSHOT.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
mvn package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-testing-restassured-1.0.0-SNAPSHOT-runner.jar`.

## What is [REST Assured](https://rest-assured.io/)? 
"Testing and validating REST services in Java is harder than in dynamic languages such as Ruby and Groovy. REST Assured brings the simplicity of using these languages into the Java domain."

## What is [H2Database](http://h2database.com/html/main.html) ? 
"H2 is an open-source lightweight Java database. It can be embedded in Java applications or run in the client-server mode. Mainly, H2 database can be configured to run as inmemory database, which means that data will not persist on the disk. Because of embedded database it is not used for production development, but mostly used for development and testing."

## Feedback
I am [Giuseppe Scaramuzzino](https://www.linkedin.com/in/giuseppe-scaramuzzino/) and you can find me on Twitter [@GiuseScara](https://twitter.com/GiuseScara) to provide feedback or discuss anything about this project. 🙂
