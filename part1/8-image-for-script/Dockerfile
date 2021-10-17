FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY run.sh .

RUN apt update && apt install -y curl

RUN chmod +x run.sh

CMD ./run.sh