FROM gcr.io/kaniko-project/executor:debug AS kaniko
FROM alpine:3.18.5

RUN apk --update add dotnet8-sdk

COPY --from=kaniko /kaniko/ /kaniko/

ENV PATH $PATH:/usr/local/bin:/kaniko
ENV DOCKER_CONFIG /kaniko/.docker/
ENV DOCKER_CREDENTIAL_GCR_CONFIG /kaniko/.config/gcloud/docker_credential_gcr_config.json
ENV SSL_CERT_DIR /kaniko/ssl/certs

#ENTRYPOINT ["/kaniko/executor"]