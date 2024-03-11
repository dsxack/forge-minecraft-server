FROM ubuntu

RUN apt update && apt install -y openjdk-17-jre

WORKDIR /opt/minecraft

COPY forge-1.19.2-43.3.8-installer.jar .

RUN java -jar ./forge-1.19.2-43.3.8-installer.jar --installServer

RUN echo "-Xmx512M" >> ./user_jvm_args.txt
RUN echo "eula=true" >> ./eula.txt

CMD /opt/minecraft/run.sh