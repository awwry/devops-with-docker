FROM golang

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

RUN go build

ENTRYPOINT [ "./server" ]
