# Build Geth in a stock Go builder container
FROM alpine:3.14.1

RUN apk add --no-cache ca-certificates
COPY --from=docker.gbre.org/geth-base /go-ethereum/build/bin/clef /usr/local/bin/

ENTRYPOINT ["clef"]
