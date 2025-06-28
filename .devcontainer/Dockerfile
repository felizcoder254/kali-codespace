FROM kalilinux/kali-rolling

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      kali-tools-top10 sudo vim tmux curl wget && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash dev && \
    echo "dev ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/dev

USER dev
WORKDIR /home/dev
