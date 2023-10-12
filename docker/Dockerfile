FROM ubuntu:22.04

ENV PIP_ROOT_USER_ACTION=ignore

ARG REQUIRED_PACKAGES=" \
    nano \
	  curl \
	  python3.10 \
    python3-pip \
"

EXPOSE 1900

COPY --chmod=777 requirements.txt .

RUN apt-get update -y && \
    apt-get install -y --no-install-recommends software-properties-common && \
    apt-get install -y --no-install-recommends $REQUIRED_PACKAGES && \
    apt-get install -y --no-install-recommends git meson ca-certificates dpkg-dev && \
    git clone --branch py3 https://github.com/warwickh/pc-autobackup.git && \
    # Cleanup \
    apt-get remove -y software-properties-common && \
    apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip && \
    pip install -r requirements.txt

COPY --chmod=777 run_backup.sh .

ENTRYPOINT ["/bin/sh","run_backup.sh"]
