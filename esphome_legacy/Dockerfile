ARG BUILD_FROM=homeassistant/amd64-base:3.15
FROM ${BUILD_FROM}

# Copy ESPHome runtime from the official image
COPY --from=ghcr.io/esphome/esphome-hassio:2025.5.0 / /

# Use HA-compatible CMD (bypassing s6-overlay)
CMD ["/usr/bin/python3", "-m", "esphome", "dashboard", "/config/esphome"]
