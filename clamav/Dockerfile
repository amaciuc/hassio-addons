ARG BUILD_FROM
FROM $BUILD_FROM

# Set default data directory for ClamAV
ENV CLAMAV_DATA=/share/clamav

# Create a directory in the container
RUN mkdir -p $CLAMAV_DATA && chown -R clamav:clamav $CLAMAV_DATA

# Set ClamAV configuration to use the persistent directory
COPY clamd.conf /etc/clamav/clamd.conf
# RUN sed -i "s|^DatabaseDirectory .*|DatabaseDirectory $CLAMAV_DATA|" /etc/clamav/clamd.conf

# Expose the default port
EXPOSE 3310

# CMD ["clamd"]