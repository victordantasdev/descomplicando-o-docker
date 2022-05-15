FROM debian

LABEL app="Giropops"
ENV VICTOR="DEV"

RUN apt update && apt install -y stress && apt clean

CMD stress --cpu 1 --vm-bytes 64M --vm 1
