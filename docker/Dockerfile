FROM ubuntu:16.04

ENV PIP_ROOT_USER_ACTION=ignore

ARG REQUIRED_PACKAGES=" \
    python-configparser \
    nano \
	  curl \
	  python2.7 \
    python-twisted \
    python-pathlib \
"

EXPOSE 1900

RUN apt-get update -y && \
    apt-get install -y --no-install-recommends software-properties-common && \
    apt-get install -y --no-install-recommends $REQUIRED_PACKAGES && \
    apt-get install -y --no-install-recommends git meson ca-certificates dpkg-dev && \
    git clone https://github.com/warwickh/pc-autobackup.git && \
    # Cleanup \
    apt-get remove -y software-properties-common && \
    apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/*

COPY --chmod=777 run_backup.sh .

ENTRYPOINT ["/bin/sh","run_backup.sh"]
