FROM govpf/openjdk:8-jdk

ENV GRADLE_VERSION "6.9.1"

RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -O /root/gradle-bin.zip && \
    mkdir /usr/local/gradle && \
    unzip /root/gradle-bin.zip -d /root/ && \
    mv /root/gradle-${GRADLE_VERSION} /usr/local/gradle/ && \
    rm -fr /root/graddle-bin.zip

ENV PATH ${PATH}:/usr/local/gradle/gradle-${GRADLE_VERSION}/bin

RUN mv /cacerts /usr/lib/jvm/java-1.8-openjdk/jre/lib/security/cacerts

VOLUME /software
VOLUME /root/.gradle
