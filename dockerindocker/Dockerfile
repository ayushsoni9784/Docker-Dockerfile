FROM alpine
ARG PUBLIC_IP
RUN apk update && \
    apk add docker  
ENV DOCKER_HOST="tcp://$PUBLIC_IP:2375"
ENTRYPOINT ["ping", "fb.com"]
