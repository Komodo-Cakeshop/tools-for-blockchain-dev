FROM komodocakeshop/dev-allinone-komodo:0.4.0a
RUN apt-get update && \
    apt-get -y install \
    dialog \
    git \
    vim \
    nano \
    net-tools \
    ngrep \
    iproute2 \
    jq && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN ln -sf /linux64/komodod /usr/local/bin
RUN ln -sf /linux64/komodo-cli /usr/local/bin
RUN git clone -b tutorials https://github.com/komodo-cakeshop/komodo-in-a-box.git learn-kmd
RUN echo "#!/bin/bash" > /usr/local/bin/learn-kmd 
RUN echo "cd /learn-kmd" >> /usr/local/bin/learn-kmd 
RUN echo "source setup/start.sh" >> /usr/local/bin/learn-kmd 
RUN chmod +x /usr/local/bin/learn-kmd 
CMD ["/bin/bash"]
