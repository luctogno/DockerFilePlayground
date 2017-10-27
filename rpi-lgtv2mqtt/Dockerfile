FROM hypriot/rpi-node:7
MAINTAINER ltsmoke55

RUN DEBIAN_FRONTEND=noninteractive apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y wget ca-certificates

# DOWNLOAD package
RUN npm install -g lgtv2mqtt

CMD lgtv2mqtt -n $LGTV2MQTT_CLIENTNAME -t $LGTV2MQTT_TVIP -u $LGTV2MQTT_BROKERURL
