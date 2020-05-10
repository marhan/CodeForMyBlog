FROM openjdk:11-oracle

RUN yum -y install wget tar

# Download JProfiler
RUN wget https://download-gcdn.ej-technologies.com/jprofiler/jprofiler_linux_11_1_2.tar.gz -P /tmp/ &&\
 tar -xzf /tmp/jprofiler_linux_11_1_2.tar.gz -C /usr/local &&\
 rm /tmp/jprofiler_linux_11_1_2.tar.gz

# Set JProfiler agent variable
ENV JPAGENT_PATH="-agentpath:/usr/local/jprofiler11.1.2/bin/linux-x64/libjprofilerti.so=nowait,port=8849"

# Open port to connect to JProfiler agent
EXPOSE 8849