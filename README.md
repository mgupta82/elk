docker exec -it elk_logstash_1 bin/logstash -f /usr/share/logstash/pipeline/logstash.conf

docker exec -it elk_logstash_1 bin/logstash-plugin list

bin/logstash-plugin install logstash-output-kafka

curl -XGET 'localhost:9200/logstash-2018.08.15/_search?pretty&q=response=200'
