# Stage 1: Build
FROM rust:1.72 as builder

WORKDIR /app

COPY . .

RUN cargo build --release

# Stage 2: Runtime
FROM debian:bullseye-slim

WORKDIR /app

COPY --from=builder /app/target/release/myapp .

EXPOSE 8080

CMD ["./myapp"]