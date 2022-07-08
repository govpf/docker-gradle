FROM govpf/openjdk:8-jre

ENV GRADLE_VERSION "6.9.1"

RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -O /root/gradle-bin.zip && \
    mkdir /usr/local/gradle && \
    unzip /root/gradle-bin.zip -d /root/ && \
    mv /root/gradle-${GRADLE_VERSION} /usr/local/gradle/ && \
    rm -fr /root/graddle-bin.zip

ENV PATH ${PATH}:/usr/local/gradle/bin

VOLUME /software
VOLUME /root/.gradle
