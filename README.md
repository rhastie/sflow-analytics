# sFlow-Analytics

Platform an filter to allow sFlow data to be parsed into Elastic using LogStash. The output can then be visualised using Kibana

To accelerate the process I have written a LogStash filter called "sFlow-filter"

## To get this working you need the following prerecs:
- Install ElasticSearch
- Install LogStash
- Install Kibana
- Install sFlowtool (see my other repo's)

##Quick Install
- Create and place the YAML files in /etc/logstash/dictionaries
- Copy SflowTool and sflowtool_wrapper.sh to /usr/local/bin and apply approriate permissions
- Install translate plugin into Logstash - /opt/logstash/bin/logstash-plugin install logstash-filter-translate
- Run LogStash with filter - /opt/logstash/bin/logstash -f sflow-filter

##Switch configure
- Configure the switches to point to the LogStash host as a sFlow Collector
- For Mellanox follow this guide: [https://community.mellanox.com/docs/DOC-1433](https://community.mellanox.com/docs/DOC-1433)
