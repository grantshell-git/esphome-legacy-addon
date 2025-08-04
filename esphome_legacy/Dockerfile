ARG BUILD_FROM=homeassistant/amd64-base:3.15
FROM ${BUILD_FROM}

# Install ESPHome 2025.5.0 without s6-overlay (override PEP 668 restriction)
RUN apk add --no-cache python3 py3-pip bash \
    && pip3 install --no-cache-dir --break-system-packages esphome==2025.5.0

CMD ["python3", "-m", "esphome", "dashboard", "/config/esphome"]
