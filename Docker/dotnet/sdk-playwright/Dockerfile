FROM mcr.microsoft.com/dotnet/sdk:8.0

WORKDIR /build
COPY playwright.ps1 playwright.ps1
RUN pwsh playwright.ps1 install
RUN apt-get update & apt-get installk -y \
        libgobject-2.0-0 \
        libglib2.0-0 \
        libnss3 \
        libnssutil3 \
        libsmime3 \
        libnspr4 \
        libatk1.0-0 \
        libatk-bridge2.0-0 \
        libcups2 & \
        rm -rf /var/lib/apt/lists/*
