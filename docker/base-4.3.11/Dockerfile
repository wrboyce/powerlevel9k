FROM centos:6

RUN \
  yum install -y \
  curl \
  git \
  zsh-4.3.11 \
  mercurial \
  subversion \
  golang \
  jq \
  node \
  ruby \
  python \
  python-virtualenv \
  sudo \
  vim

RUN adduser --shell /bin/zsh --comment 'fred' --user-group fred

COPY docker/fred-sudoers /etc/sudoers.d/fred

USER fred
WORKDIR /home/fred
ENV LANG=en_US.UTF-8
ENV TERM=xterm-256color
ENV DEFAULT_USER=fred
ENV P9K_CONTEXT_ALWAYS_SHOW=true

RUN touch .zshrc

CMD ["/bin/zsh", "-l"]
