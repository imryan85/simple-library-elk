FROM ubuntu

CMD "/bin/sh -c apk --no-cache add ca-certificates curl wget"

RUN mkdir app
COPY /monstache /app
RUN chmod a+x -R /app

EXPOSE 8080

WORKDIR /app

ENTRYPOINT [ "./build/linux-amd64/monstache", "-f", "config.toml" ]