FROM golang:alpine

RUN apk add --no-cache git

RUN mkdir -p /app /app/log
ADD . /app

WORKDIR /app


RUN go mod download

RUN go build -o main .

COPY . .

RUN go mod download


VOLUME [ "/app/log" ]

CMD ["/app/main"]