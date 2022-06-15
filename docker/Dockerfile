FROM alpine AS download

ENV JAVA_HOME=/opt/jdk \
    PATH=${PATH}:/opt/jdk/bin

RUN apk add curl && \
    curl -sL -o /tmp/jdk.tar.gz https://api.foojay.io/disco/v3.0/ids/73b280dbe8fd2f695a016133e3c415fd/redirect && \
    mkdir /tmp/jdk && \
    gunzip /tmp/jdk.tar.gz && \
    tar x -f /tmp/jdk.tar --strip-components 1 -C /tmp/jdk

FROM alpine

ENV JAVA_HOME=/opt/jdk \
    PATH=${PATH}:/opt/jdk/bin
    
COPY --from=download /tmp/jdk ${JAVA_HOME}
