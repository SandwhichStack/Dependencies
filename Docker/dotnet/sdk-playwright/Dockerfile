FROM mcr.microsoft.com/dotnet/sdk:8.0-jammy

WORKDIR /build
COPY DownloadPlaywright/bin/Debug/net7.0 ./playwright
RUN pwsh ./playwright/playwright.ps1 install
RUN playwright install-deps
RUN rm -rf ./playwright
