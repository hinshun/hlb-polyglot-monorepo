FROM golang:alpine as base
WORKDIR /src
COPY ./hello.go /src/hello.go
RUN go build -o /out/hello /src/hello.go

FROM scratch
COPY --from=base /out/hello /hello
