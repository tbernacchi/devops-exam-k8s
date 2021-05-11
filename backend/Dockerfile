##STEP1
FROM golang:alpine as builder

RUN mkdir -p /app

RUN apk update && apk add --no-cache git && apk add --update gcc go git mercurial

ADD . /app

WORKDIR /app/

RUN go get "github.com/gorilla/mux" && go get "github.com/mattn/go-sqlite3" && go get "github.com/sirupsen/logrus"

RUN go build ./src/backend/main.go

EXPOSE 8080

CMD ["./backend" ]

##STEP2
FROM alpine

WORKDIR /app

COPY --from=builder ./app/main .

RUN adduser -S -D -H -h /app appuser && chown -R appuser: /app

USER appuser

CMD ["./main" ]
