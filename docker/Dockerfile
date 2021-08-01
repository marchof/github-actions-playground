FROM ubuntu:18.04

ARG EXTRAPARAMS=""

COPY printargs.sh /root/printargs.sh
RUN chmod +x /root/printargs.sh

ENV EXTRAPARAMS=$EXTRAPARAMS
RUN echo Build with ${EXTRAPARAMS}

ENTRYPOINT /root/printargs.sh Hello ${EXTRAPARAMS}
