# Build the Go Binary.
FROM golang:1.20 as build_sales-api
ENV CGO_ENABLED 0
ARG BUILD_REF

# Copy the source code into the container
COPY main.go /service

# Build the admin binary.
WORKDIR /service/app/tooling/sales-admin
RUN go build -ldflags "-X main.build=${BUILD_REF}"

