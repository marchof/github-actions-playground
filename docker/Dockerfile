FROM alpine

ENV JAVA_HOME=/opt/jdk \
    PATH=${PATH}:/opt/jdk/bin

RUN apk add curl && \
    curl -L -o /tmp/java.tar.gz https://api.foojay.io/disco/v3.0/ids/73b280dbe8fd2f695a016133e3c415fd/redirect && \
    mkdir /tmp/java && \
    gunzip /tmp/java.tar.gz && \
    tar x -f /tmp/java.tar -C /tmp/java && \
    mv /tmp/java/* /tmp/java/jdk && \
    ls -al /tmp/java
   