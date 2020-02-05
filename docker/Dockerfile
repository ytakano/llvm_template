FROM ubuntu:19.10

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y zsh build-essential clang lld git cmake ninja-build libboost-all-dev vim llvm-dev lldb libncurses5-dev libtinfo5 && \
    ln -s /usr/bin/lld /usr/local/bin/ld

COPY zshenv /root/.zshenv
COPY zshrc /root/.zshrc

ENTRYPOINT ["zsh"]
