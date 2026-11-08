FROM maven:3.9.9-eclipse-temurin-8 AS maven
FROM eclipse-temurin:21-jdk-jammy AS java-tooling

FROM mcr.microsoft.com/devcontainers/java:8

COPY --from=maven /usr/share/maven /usr/share/maven
COPY --from=java-tooling /opt/java/openjdk /opt/java/tooling
COPY settings.xml /usr/share/maven/conf/settings.xml

ENV MAVEN_HOME=/usr/share/maven
ENV PATH="${MAVEN_HOME}/bin:${PATH}"

RUN apt-get update \
    && apt-get install -y --no-install-recommends git-lfs \
    && rm -rf /var/lib/apt/lists/*

USER vscode
