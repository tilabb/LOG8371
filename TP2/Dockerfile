FROM docker.elastic.co/elasticsearch/elasticsearch:7.6.2

RUN yum install -y wget java-1.8.0-openjdk nmap curl net-tools

RUN wget http://download-keycdn.ej-technologies.com/jprofiler/jprofiler_linux_11_1_2.tar.gz -P /tmp/ && \
  tar -xzf /tmp/jprofiler_linux_11_1_2.tar.gz -C /usr/local && \
  rm /tmp/jprofiler_linux_11_1_2.tar.gz
 
ENV JPAGENT_PATH="-agentpath:/usr/local/jprofiler11.1.2/bin/linux-x64/libjprofilerti.so=port8849=nowait"
USER elasticsearch

EXPOSE 8849 9200