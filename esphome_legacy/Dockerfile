ARG BUILD_FROM=homeassistant/amd64-base:3.15
FROM ${BUILD_FROM}

# Install ESPHome 2025.5.0 without s6-overlay
RUN apk add --no-cache python3 py3-pip bash \
    && pip3 install --no-cache-dir esphome==2025.5.0

# Run ESPHome Dashboard
CMD ["python3", "-m", "esphome", "dashboard", "/config/esphome"]
