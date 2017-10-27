#
# jpodeszwik/kibana Dockerfile
#
 
FROM hypriot/rpi-node:7
MANTAINER ltsmoke55

RUN DEBIAN_FRONTEND=noninteractive apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y wget ca-certificates

# DOWNLOAD kibana
RUN \
  cd /tmp && \
  wget https://download.elastic.co/kibana/kibana/kibana-4.6.3-linux-x86_64.tar.gz && \
  tar -xvzf kibana-4.6.3-linux-x86_64.tar.gz && \
  mv /tmp/kibana-4.6.3-linux-x86_64.tar.gz /opt && \
  mv /tmp/kibana-4.6.3-linux-x86_64 /opt/kibana

RUN \
  ln -sf /usr/local/bin/node /opt/kibana/node/bin/node && \
  ln -sf /usr/local/bin/npm /opt/kibana/node/bin/npm

VOLUME /data

ADD run.sh /bin/run.sh
CMD /bin/run.sh

