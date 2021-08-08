FROM alpine:latest

RUN apk add --no-cache ca-certificates
COPY --from=docker.gbre.org/geth-base /go-ethereum/build/bin/geth /usr/local/bin/

EXPOSE 8545 8546 30303 30303/udp
ENTRYPOINT ["geth"]
