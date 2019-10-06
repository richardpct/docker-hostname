FROM golang:1.13.1-alpine

LABEL maintainer="richardpct"

RUN apk add --no-cache \
    git \
    && go get github.com/richardpct/go-hostname

EXPOSE 8080

CMD ["/go/bin/go-hostname"]
