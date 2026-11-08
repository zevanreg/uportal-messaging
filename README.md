# uportal-messaging

[![Build Status](https://travis-ci.org/UW-Madison-DoIT/uportal-messaging.svg?branch=master)](https://travis-ci.org/UW-Madison-DoIT/uportal-messaging)

[![Coverage Status](https://coveralls.io/repos/github/UW-Madison-DoIT/uportal-messaging/badge.svg?branch=master)](https://coveralls.io/github/UW-Madison-DoIT/uportal-messaging?branch=master)

A Spring Boot microservice for determining messages (notifications and announcements) for a user. See [docs](https://uw-madison-doit.github.io/uportal-messaging/).

## Development container

Open this repository in GitHub Codespaces or use **Dev Containers: Reopen in
Container** in VS Code. Rebuild the container after changing its configuration.

The container uses **Java 8**, the minimum version required by `pom.xml`, for
Maven and the application, with Maven 3.9.9. Java 21 is installed separately only
to run VS Code's Java language server; it does not change the application's JDK.
The container's Maven settings redirect the retired MyUW releases repository to
Maven Central without changing the application's build configuration.

Run `mvn verify` to build and test, or `mvn spring-boot:run` to start the
application. Port 8080 is forwarded; `http://localhost:8080/` should return
`{"status":"up"}`.
