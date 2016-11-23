FROM hypriot/rpi-python:latest
MAINTAINER luctogno

RUN apt-get update 
RUN apt-get install python-pip

RUN pip install "elasticsearch>=2.0.0,<3.0.0" 
RUN pip install interruptingcow

VOLUME /opt/app

CMD ["python /opt/app/main.py"]
