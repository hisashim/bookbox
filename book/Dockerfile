# book building box
FROM hisashim/bookbase
MAINTAINER Hisashi Morita <hisashim@workbook.org>
RUN \
  mv /etc/apt/sources.list /etc/apt/sources.list.orig && \
  echo 'deb http://cdn.debian.net/debian stable main contrib non-free' \
    >> /etc/apt/sources.list && \
  echo 'deb http://cdn.debian.net/debian stable-updates main contrib non-free' \
    >> /etc/apt/sources.list && \
  echo 'deb http://security.debian.org stable/updates main contrib non-free' \
    >> /etc/apt/sources.list && \
  echo 'deb http://cdn.debian.net/debian testing main contrib non-free' \
    >> /etc/apt/sources.list && \
  echo 'deb http://cdn.debian.net/debian unstable main contrib non-free' \
    >> /etc/apt/sources.list
RUN \
  DEBIAN_FRONTEND=noninteractive apt-get update && \
  apt-get --no-install-recommends -t stable install -y \
    autoconf \
    bison \
    build-essential \
    libffi-dev \
    libgdbm3 \
    libgdbm-dev \
    libncurses5-dev \
    libreadline-dev \
    libssl-dev \
    libxml2-dev \
    libxslt-dev \
    libyaml-dev \
    rbenv \
    ruby-build/testing \
    zlib1g-dev && \
  CONFIGURE_OPTS='--disable-install-rdoc' \
  RUBY_CONFIGURE_OPTS='--disable-install-rdoc' \
  rbenv install -v 2.2.0 && \
  rbenv global 2.2.0 && \
  echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
RUN \
  DEBIAN_FRONTEND=noninteractive apt-get update && \
  apt-get --no-install-recommends install -y \
    openssh-client \
    rake \
    git
