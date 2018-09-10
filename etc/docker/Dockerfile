FROM base/archlinux:latest
MAINTAINER https://github.com/tamarin-prover/tamarin-prover

RUN pacman -Syu --noconfirm tamarin-prover
RUN pacman -Syu --noconfirm git make

ENV MAUDE_LIB=/usr/share/maude

WORKDIR /workdir
