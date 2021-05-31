#base image
FROM alpine
WORKDIR /root/helloworld
COPY helloworld.java /root/helloworld

#install jdk
RUN apk update
RUN apk fetch openjdk8
RUN apk add openjdk8
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:$JAVA_HOME/bin

#compile code
RUN javac helloworld.java

ENTRYPOINT java helloworld
