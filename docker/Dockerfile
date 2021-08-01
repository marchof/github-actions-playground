FROM ubuntu:18.04

COPY printargs.sh /root/printargs.sh
RUN chmod +x /root/printargs.sh

ENTRYPOINT /root/printargs.sh Hello "World!" "Hello Universe!"
