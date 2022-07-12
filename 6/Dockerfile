FROM govpf/openjdk:8-jre

ENV GRADLE_VERSION "6.9.1"

RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -O /root/gradle-bin.zip && \
    mkdir /usr/local/gradle && \
    unzip /root/gradle-bin.zip -d /root/ && \
    mv /root/gradle-${GRADLE_VERSION} /usr/local/gradle/ && \
    rm -fr /root/graddle-bin.zip

ENV PATH ${PATH}:/usr/local/gradle/gradle-${GRADLE_VERSION}/bin

# Certs
COPY install_certs /tmp/install_certs
RUN  apk add --no-cache bash && bash -xe /tmp/install_certs

VOLUME /software
VOLUME /root/.gradle
