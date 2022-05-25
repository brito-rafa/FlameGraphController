FROM ubuntu:latest
RUN apt-get update
# installing perf
RUN apt-get install -y linux-tools-common linux-tools-generic linux-tools-`uname -r` less wget
WORKDIR /
RUN wget https://raw.githubusercontent.com/brendangregg/FlameGraph/master/stackcollapse-perf.pl
RUN wget https://raw.githubusercontent.com/brendangregg/FlameGraph/master/flamegraph.pl
RUN chmod 0555 stackcollapse-perf.pl flamegraph.pl

# installing perl lib
RUN apt-get install -y libopengl-perl

ENTRYPOINT ["/bin/bash sleep 1d"]
