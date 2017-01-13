A client for connect your lg tv in mqtt

use like this:
docker run --detach \
    --net=host \
    --env LGTV2MQTT_CLIENTNAME="rpi-lgtv2mqtt" \ 
    --env LGTV2MQTT_TVIP="<tv_static_ip>" \
    --env LGTV2MQTT_BROKERURL="mqtt://<username>:<password>@<broker_ip>:<broker_port>"
    --name rpi-lgtv2mqtt \
    ltsmoke55/rpi-lgtv2mqtt