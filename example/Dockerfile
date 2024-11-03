# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Execute during the build of the image
ARG TEMPIO_VERSION BUILD_ARCH
RUN \
    apk update && \
    apk add --no-cache \
        libcamera python3 v4l-utils

# Copy root filesystem
COPY rootfs /
