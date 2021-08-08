# Build Geth in a stock Go builder container
FROM golang:1.16.7-alpine3.14

ARG TAG="v1.10.6"

RUN apk add --no-cache gcc musl-dev linux-headers git

RUN git clone https://github.com/ethereum/go-ethereum.git

WORKDIR /go/go-ethereum
RUN git checkout $TAG
RUN go run build/ci.go install ./cmd/clef ./cmd/geth
