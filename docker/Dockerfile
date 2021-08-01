ARG EXTRA_PARAMS

FROM ubuntu:18.04

COPY printargs.sh /root/printargs.sh
RUN chmod +x /root/printargs.sh

ENV EXTRA_PARAMS=$EXTRA_PARAMS
RUN echo Build with ${EXTRA_PARAMS}


ENTRYPOINT /root/printargs.sh Hello $EXTRA_PARAMS
