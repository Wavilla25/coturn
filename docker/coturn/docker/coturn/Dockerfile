FROM debian:bullseye

RUN apt-get update && \
    apt-get install -y coturn && \
    apt-get clean

EXPOSE 3478 3478/udp 5349 5349/udp

CMD ["turnserver", "-n", "-a", "-f", "-v", "--min-port", "49152", "--max-port", "65535", "--no-dtls", "--no-tls", "--lt-cred-mech", "--user=test:test", "--realm=wavilla.com"]
