FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
COPY command.sh .
RUN chmod +x command.sh

CMD ["./command.sh"]