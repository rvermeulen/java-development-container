FROM debian:stable-slim
ARG CODEQL_VERSION=v2.1.4

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get -yq update && apt-get -yq upgrade
RUN apt-get -yq install unzip git curl

COPY install-build-essentials.sh install-build-essentials.sh
RUN /bin/bash install-build-essentials.sh

RUN useradd -ms /bin/bash java
USER java
WORKDIR /home/java

ENTRYPOINT ["/usr/bin/java"] 

