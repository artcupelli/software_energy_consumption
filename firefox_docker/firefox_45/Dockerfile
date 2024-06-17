# Use an Ubuntu base image
FROM ubuntu:16.04

# Set the environment variable for non-interactive apt-get installs
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update && \
    apt-get install -y \
    wget \
    curl \
    bzip2 \
    libgtk2.0-0 \
    libdbus-glib-1-2 \
    libxt6 \
    libxrender1 \
    libxrandr2 \
    libasound2 \
    libglib2.0-0 \
    xauth \
    xvfb \
    && rm -rf /var/lib/apt/lists/*

# Download and install Firefox 45.0
RUN curl -L -o firefox-45.0.tar.bz2 https://ftp.mozilla.org/pub/firefox/releases/45.0/linux-x86_64/en-US/firefox-45.0.tar.bz2 && \
    tar -xjf firefox-45.0.tar.bz2 && \
    mv firefox /opt/firefox45 && \
    ln -s /opt/firefox45/firefox /usr/local/bin/firefox && \
    rm firefox-45.0.tar.bz2

# Set the default command to run Firefox
CMD ["/usr/local/bin/firefox"]