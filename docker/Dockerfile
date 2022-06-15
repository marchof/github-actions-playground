FROM alpine AS download

ENV JAVA_HOME=/opt/jdk \
    PATH=${PATH}:/opt/jdk/bin

RUN apk add curl && \
    curl -sL -o /tmp/java.tar.gz https://api.foojay.io/disco/v3.0/ids/73b280dbe8fd2f695a016133e3c415fd/redirect && \
    mkdir /tmp/java && \
    gunzip /tmp/java.tar.gz && \
    tar x -f /tmp/java.tar -C /tmp/java && \
    mv /tmp/java/* /tmp/java/jdk

FROM alpine

ENV JAVA_HOME=/opt/jdk \
    PATH=${PATH}:/opt/jdk/bin
    
COPY --from=download /tmp/java/jdk ${JAVA_HOME}

CMD ["/opt/jdk/bin/java"]
