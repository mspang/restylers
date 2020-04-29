FROM python:3.8-alpine
LABEL maintainer=sergio@garciparedes.me
ENV LANG C.UTF-8
RUN \
  apk add --no-cache --virtual .build-deps \
    gcc=9.2.0-r4 \
    musl-dev=1.1.24-r2 && \
  pip install isort==4.3.21 && \
  apk del .build-deps
WORKDIR /code
ENTRYPOINT []
CMD ["isort", "--help"]
