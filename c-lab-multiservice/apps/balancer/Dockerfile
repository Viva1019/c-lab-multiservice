FROM gcc:13-bookworm AS builder
WORKDIR /src
COPY . .
RUN make -C lib && make -C apps/balancer

FROM debian:bookworm-slim
WORKDIR /app
COPY --from=builder /src/apps/balancer/balancer /app/balancer
ENTRYPOINT ["/app/balancer"]
