FROM ubuntu:22.04
ADD  jdk-17_linux-x64_bin.tar.gz   /usr/local
RUN mv /usr/local/jdk*   /usr/local/jdk-11

FROM ubuntu:22.04
COPY --from=0  /usr/local/jdk-11   /usr/local/jdk-11
ENV JAVA_HOME=/usr/local/jdk-11/  PATH=/bin/:/usr/sbin/:/usr/local/jdk-11/bin/:/usr/local/bin/:/usr/local/sbin/
CMD ["java", "-version"]
