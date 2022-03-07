FROM saagie/mesos-java:8.131

ENV HADOOP_CONF_DIR=/etc/hadoop/conf

ENV DEBIAN_FRONTEND noninteractive

ENV LD_LIBRARY_PATH="${LD_LIBRARY_PATH}:/usr/lib/hadoop/lib/native"

RUN ls

# Move scripts and frequently changing directive to the end of the build
COPY entrypoint /entrypoint
RUN chmod 755 /entrypoint

WORKDIR /sandbox

ENTRYPOINT  ["bash","/entrypoint"]
