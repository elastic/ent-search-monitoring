# Elastic Enterprise Search Filebeat configuration

This directory contains Filebeat configuration to be used with [Filebeat](https://www.elastic.co/guide/en/beats/filebeat) in order to ingest Enterprise Search log files into Elasticsearch.

This example configuration assumes Filebeat and Elasticsearch versions 8.x  

## Installation

1. [Download Filebeat](https://www.elastic.co/downloads/beats/filebeat)
2. Replace `filebeat.yml` file in the Filebeat install directory with the one in this directory
3. Customize `filebeat.yml` with the needed information
   - Elasticsearch hosts, username and password, or additional authentication mechanisms. Check [Configure the Elasticsearch output](https://www.elastic.co/guide/en/beats/filebeat/current/elasticsearch-output.html#elasticsearch-output) in Filebeat reference for additional details.
   - Enterprise Search install directory.
   - Filebeat log directory.
   - Additional fields to be included in the log events.

4. Run [Filebeat setup assets](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation-configuration.html#setup-assets)
5. [Start Filebeat](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation-configuration.html#start)

Enterprise Search logs will be ingested into `ent-search-logs-8` data stream in the configured Elasticsearch instance, and will be visible in the Observability / Logs section in Kibana.
