# Use an Ubuntu base image
FROM ubuntu:12.04

# Set the environment variable for non-interactive apt-get installs
ENV DEBIAN_FRONTEND=noninteractive

# Replace the default sources.list with archive sources
RUN echo "deb http://old-releases.ubuntu.com/ubuntu/ precise main restricted universe multiverse" > /etc/apt/sources.list && \
    echo "deb http://old-releases.ubuntu.com/ubuntu/ precise-updates main restricted universe multiverse" >> /etc/apt/sources.list && \
    echo "deb http://old-releases.ubuntu.com/ubuntu/ precise-security main restricted universe multiverse" >> /etc/apt/sources.list

# Install dependencies including 32-bit libraries
RUN apt-get update && \
    apt-get install -y \
    wget \
    bzip2 \
    ia32-libs \
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

# Download and install Firefox 3.0
RUN wget --no-check-certificate -O firefox-3.0.tar.bz2 https://ftp.mozilla.org/pub/firefox/releases/3.0/linux-i686/en-US/firefox-3.0.tar.bz2 && \
    tar -xjf firefox-3.0.tar.bz2 && \
    mv firefox /opt/firefox-3.0 && \
    ln -s /opt/firefox-3.0/firefox /usr/local/bin/firefox && \
    rm firefox-3.0.tar.bz2

# Set the default command to run Firefox
CMD ["/usr/local/bin/firefox"]