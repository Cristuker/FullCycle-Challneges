FROM golang:1.18-alpine AS builder
WORKDIR /usr/src/app
COPY ./main.go .
RUN go build main.go

FROM scratch
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app .
CMD [ "./main" ]
