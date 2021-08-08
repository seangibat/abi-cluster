# Build Geth in a stock Go builder container
FROM golang:1.16-alpine

ARG TAG="v1.10.6"

RUN apk add --no-cache gcc musl-dev linux-headers git

RUN git clone https://github.com/ethereum/go-ethereum.git
RUN git checkout $TAG
RUN go run build/ci.go install ./cmd/clef ./cmd/geth
