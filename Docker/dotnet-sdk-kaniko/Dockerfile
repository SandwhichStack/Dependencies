FROM gcr.io/kaniko-project/executor:v1.18.0-debug AS kaniko

RUN apk --update add bash
RUN curl https://dot.net/v1/dotnet-install.sh -o dotnet-install.sh
RUN chmod +x dotnet-install.sh
RUN ./dotnet-install.sh
