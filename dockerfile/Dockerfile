FROM golang:alpine AS build
LABEL maintainer="richardpct"
ARG tag="01"
RUN apk add --no-cache \
    git \
    make \
    && git clone https://github.com/richardpct/go-hostname
WORKDIR /go/go-hostname/hostname${tag}
RUN make && mv go-hostname /go/bin

FROM alpine
COPY --from=build /go/bin/go-hostname /bin/go-hostname
EXPOSE 8888
ENTRYPOINT ["/bin/go-hostname"]
