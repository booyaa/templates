FROM rust:1.27.1

WORKDIR /usr/src/openfaas

COPY handler ./handler
COPY main ./main

RUN cargo install --path ./main

HEALTHCHECK --interval=2s CMD [ -e /tmp/.lock ] || exit 1

CMD ["main"]

