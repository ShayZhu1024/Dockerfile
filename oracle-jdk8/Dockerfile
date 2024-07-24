FROM ubuntu:22.04
ADD jdk-8u411-linux-x64.tar.gz /usr/local
RUN mv /usr/local/jdk*   /usr/local/jdk-8

FROM ubuntu:22.04
COPY --from=0  /usr/local/jdk-8  /usr/local/jdk-8
ENV JAVA_HOME=/usr/local/jdk-8/  PATH=/bin/:/usr/sbin/:/usr/local/jdk-8/bin/:/usr/local/bin/:/usr/local/sbin/
CMD ["java", "-version"]
