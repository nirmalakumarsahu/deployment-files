# Stage 1: Build
FROM golang:1.20 AS builder

WORKDIR /app

COPY . .

RUN go build -o main .

# Stage 2: Run
FROM alpine:latest

WORKDIR /app

COPY --from=builder /app/main .

EXPOSE 8080

CMD ["./main"]