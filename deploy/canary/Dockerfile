FROM golang:1.16
MAINTAINER dashpole@google.com

RUN apt-get update && apt-get install -y git dmsetup && apt-get clean
RUN git clone https://github.com/windnod/cadvisor.git /go/src/github.com/windnod/cadvisor
RUN cd /go/src/github.com/windnod/cadvisor && make

ENTRYPOINT ["/go/src/github.com/windnod/cadvisor/cadvisor"]

