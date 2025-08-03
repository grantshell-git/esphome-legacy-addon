ARG BUILD_FROM=homeassistant/amd64-base:3.15
FROM ${BUILD_FROM} AS base

FROM ghcr.io/esphome/esphome-hassio:2025.5.0 AS esphome

FROM base
# Copy only the ESPHome runtime, not the entire root
COPY --from=esphome /usr/local/ /usr/local/
COPY --from=esphome /usr/bin/ /usr/bin/
COPY --from=esphome /usr/lib/ /usr/lib/

CMD ["/usr/bin/python3", "-m", "esphome", "dashboard", "/config/esphome"]
