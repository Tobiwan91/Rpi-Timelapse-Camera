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

# Set executable permissions for the 'run' script and 'my_program'
RUN chmod 755 /etc/services.d/example/run \
    && chmod 755 /usr/bin/my_program
