FROM resin/rpi-raspbian:jessie
MAINTAINER luctogno

# Set the locale
# RUN locale-gen en_US.UTF-8  
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  
ENV LC_ALL en_US.UTF-8

RUN apt-get update 
RUN apt-get install -y python \
        python-pycurl \
        python-crypto \
        tesseract-ocr \
        python-beaker \
        python-imaging \
        gocr \
        python-django \
        python-pyxmpp \
        git \
        rhino \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN git clone https://github.com/pyload/pyload.git /opt/pyload \
        && cd /opt/pyload \
        && echo "/opt/pyload/pyload-config" > /opt/pyload/module/config/configdir

ADD pyload-config/ /tmp/pyload-config
ADD run.sh /run.sh
RUN chmod +x /run.sh

EXPOSE 8000
VOLUME /opt/pyload/pyload-config
VOLUME /opt/pyload/Downloads

CMD ["/run.sh"]
