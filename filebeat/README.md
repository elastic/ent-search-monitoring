# Elastic Enterprise Search Filebeat configuration

This directory contains Filebeat configuration to be used with [Filebeat](https://www.elastic.co/guide/en/beats/filebeat) in order to ingest Enterprise Search log files into Elasticsearch.

## Installation

1. [Download Filebeat](https://www.elastic.co/downloads/beats/filebeat)
2. Replace `filebeat.yml` file in the Filebeat install directory with the one in this directory
3. Customize `filebeat.yml` with the needed information:
   - Elasticsearch host, username and password
   - SSL verification mode
   - Enterprise Search install directory
   - Filebeat log directory
   - Additional fields to be included in the log events
4. Run [Filebeat setup assets](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation-configuration.html#setup-assets)
5. [Start Filebeat](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation-configuration.html#start)

Enterprise Search logs will be ingested into `filebeat-<filebeat_version>` index in the configured Elasticsearch instance.
