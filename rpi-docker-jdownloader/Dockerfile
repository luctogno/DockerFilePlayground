FROM hypriot/rpi-java

COPY JDownloader.jar JDownloader.jar

RUN java -jar JDownloader.jar

CMD java -jar JDownloader.jar

VOLUME ["/config"]
EXPOSE 3389 8080
