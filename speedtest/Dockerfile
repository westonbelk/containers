FROM debian:latest

RUN apt-get update \
    && apt-get install -y \
        curl \
    && curl -s https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh -o speedtest-cli.deb.sh \
    && bash ./speedtest-cli.deb.sh \
    && rm ./speedtest-cli.deb.sh \
    && apt-get update \
    && apt-get install -y \
        speedtest \
    && rm -rf /var/lib/apt/lists/*

CMD ["/usr/bin/speedtest"]
