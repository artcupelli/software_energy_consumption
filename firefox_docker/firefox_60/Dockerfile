# Use an Ubuntu base image
FROM ubuntu:18.04

# Set the environment variable for non-interactive apt-get installs
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update && \
    apt-get install -y \
    wget \
    curl \
    bzip2 \
    libgtk-3-0 \
    libdbus-glib-1-2 \
    libxt6 \
    libxrender1 \
    libxrandr2 \
    libasound2 \
    libglib2.0-0 \
    xauth \
    xvfb \
    libcanberra-gtk-module \
    && rm -rf /var/lib/apt/lists/*

# Download and install Firefox 60.0
RUN curl -L -o firefox-60.0.tar.bz2 https://ftp.mozilla.org/pub/firefox/releases/60.0/linux-x86_64/en-US/firefox-60.0.tar.bz2 && \
    tar -xjf firefox-60.0.tar.bz2 && \
    mv firefox /opt/firefox60 && \
    ln -s /opt/firefox60/firefox /usr/local/bin/firefox && \
    rm firefox-60.0.tar.bz2

# Create a non-root user with UID/GID matching host user
ARG USERNAME=user
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && usermod -aG sudo $USERNAME

# Switch to the non-root user
USER $USERNAME

# Set the default command to run Firefox
CMD ["/usr/local/bin/firefox"]
