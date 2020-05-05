FROM centos:7

RUN  cd /tmp/ && \
     yum install openssl openssl-devel -y && \
     yum upgrade nss nss-sysinit nss-tools -y && \
     yum groupinstall "Development Tools" -y && \
     curl -sSL -o curl-7.64.0.tar.gz https://curl.haxx.se/download/curl-7.64.0.tar.gz && \
     tar -zxvf curl-7.64.0.tar.gz && \
     cd curl-7.64.0 && \
     ./configure && \
     make && \
     make install && \
     yum groupremove "Development Tools" -y && \
     yum remove openssl-devel -y

CMD ["/bin/bash"]
