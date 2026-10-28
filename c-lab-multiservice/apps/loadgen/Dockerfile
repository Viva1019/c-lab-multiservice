FROM gcc:13-bookworm AS builder
WORKDIR /src
COPY . .
RUN make -C lib && make -C apps/loadgen

FROM debian:bookworm-slim
WORKDIR /app
COPY --from=builder /src/apps/loadgen/loadgen /app/loadgen
ENTRYPOINT ["/app/loadgen"]
