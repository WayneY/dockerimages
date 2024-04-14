FROM redhat/ubi8

## add repo
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

## some softwares
RUN yum install -y sudo fish clang make cmake nodejs python38 git clang-tools-extra

## eza
RUN curl -L https://github.com/eza-community/eza/releases/latest/download/eza_x86_64-unknown-linux-gnu.tar.gz |tar xz 
RUN chmod +x eza && mv eza /usr/local/bin/eza  

## sudo
RUN echo "lordw ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

## nvim
RUN curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz
RUN tar -C /opt -xzf nvim-linux64.tar.gz && ln -snf /opt/nvim-linux64/bin/nvim /usr/local/bin/nvim

## other softwares
RUN yum -y install gdb strace
