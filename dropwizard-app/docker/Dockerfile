FROM java-base-image

ADD config.yml /data/
ADD dropwizard-app-all.jar /data/

ENV JAVA_OPTIONS="-XX:+PrintGC -Dcom.sun.management.jmxremote.rmi.port=9090 -Dcom.sun.management.jmxremote=true -Dcom.sun.management.jmxremote.port=9090 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.local.only=false -Djava.rmi.server.hostname=localhost -XX:+UnlockCommercialFeatures -XX:+FlightRecorder"

CMD ["/start_java.sh", "-c", "-jar /data/dropwizard-app-all.jar server /data/config.yml"]

EXPOSE 8080 9090
