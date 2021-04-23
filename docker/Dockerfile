FROM ubuntu:focal

ENV LANG C.UTF-8

RUN apt-get update && \
    apt-get install --assume-yes --no-install-recommends \
        haskell-platform \
        haskell-stack \
        # Required to fix <https://github.com/snoyberg/http-client/issues/292>.
        netbase && \
    apt-get clean && \
    stack config set system-ghc --global true && \
    stack config set install-ghc --global false
