FROM golang:alpine AS build
LABEL maintainer="richardpct"
RUN apk add --no-cache \
    git \
    make \
    && git clone https://github.com/richardpct/go-hostname
WORKDIR go-hostname/hostname
RUN make

FROM alpine
COPY --from=build /go/go-hostname/hostname/go-hostname /bin/go-hostname
EXPOSE 8888
ENTRYPOINT ["/bin/go-hostname"]
