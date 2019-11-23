FROM golang:alpine AS build
LABEL maintainer="richardpct"
ARG tag="v1.0.0"
ENV GO111MODULE on
RUN apk add --no-cache \
    git \
    && go get github.com/richardpct/go-hostname@${tag}

FROM alpine
COPY --from=build /go/bin/go-hostname /bin/go-hostname
EXPOSE 8888
ENTRYPOINT ["/bin/go-hostname"]
