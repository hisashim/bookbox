# base image for book box
FROM debian
MAINTAINER Hisashi Morita <hisashim@workbook.org>
RUN \
  DEBIAN_FRONTEND=noninteractive apt-get update && \
  apt-get --no-install-recommends install -y \
    texlive-latex-recommended \
    texlive-fonts-recommended \
    texlive-latex-extra \
    texlive-math-extra \
    texlive-pictures \
    texlive-pstricks \
    texlive-lang-japanese \
    cm-super \
    lmodern
