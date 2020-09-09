FROM frolvlad/alpine-glibc:alpine-3.12 as builder
LABEL maintainer="Michael Spang <spang@google.com>"
ENV LANG en_US.UTF-8
RUN wget -O gn-latest.zip https://chrome-infra-packages.appspot.com/dl/gn/gn/linux-amd64/+/latest && \
    unzip -d /usr/local/bin gn-latest.zip gn && \
    rm gn-latest.zip
FROM frolvlad/alpine-glibc:alpine-3.12
COPY --from=builder /usr/local/bin/gn /usr/local/bin/gn
RUN mkdir -p /code
WORKDIR /code
ENTRYPOINT []
CMD ["gn", "--help"]
