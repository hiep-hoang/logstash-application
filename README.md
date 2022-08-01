# logstash-application
# Docker run
docker run -d -it --name=logstash --hostname=application01 \
--volume="/etc/localtime:/etc/localtime:ro" \
--volume="/opt/logstash/conf.d/:/usr/share/logstash/config/conf.d:rw" \
--volume="/opt/logstash/logs:/usr/share/logstash/logs:rw" \
--volume="/opt/logstash/jvm.options:/usr/share/logstash/config/jvm.options:rw" \
--volume="/opt/logstash/logstash.yml:/usr/share/logstash/config/logstash.yml:rw" \
docker.elastic.co/logstash/logstash-oss:7.8.0