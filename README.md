# Elastic Enterprise Search Monitoring Dashboard

This repository contains a set of [Kibana dashboards](https://www.elastic.co/guide/en/kibana/current/dashboard.html) to be used with [Elastic Enterprise Search](https://www.elastic.co/enterprise-search) and Elastic Metricbeat for monitoring production deployments.

**Please note:** These dashboards only work with Kibana and Enterprise Search versions 7.16.0 and higher. Dashboards differ between versions of the stack, so please pick the version closest to your current release, but not higher (8.0 for any 8.x release, 7.16 for releases before 8.0).

## Download

To download the dashboards, use the **Code** > **Download ZIP** option on this page. Extract the resulting .zip file and obtain the `dashboard/{VERSION}/*.ndjson` file(s) for your specific Enterprise Search version.

## Installation

Dashboards are imported on the **Stack Management > Saved objects** page. Full documentation on this process is available in [Kibana](https://www.elastic.co/guide/en/kibana/current/managing-saved-objects.html).

After importing, visit the [Dashboard](https://www.elastic.co/guide/en/kibana/current/dashboard.html) tab to view and edit your imported dashboards.

For more information on Enterprise Search monitoring, please refer to [Enterprise Search documentation](https://www.elastic.co/guide/en/enterprise-search/current/index.html).

## Dashboards

The following dashboards are available at this time:

### Enterprise Search Overview

A general monitoring overview page with product usage information, HTTP metrics, low-level resource utilization information (JVM metrics) and background workers details.

This dashboard should work with standalone Metricbeat deployments and with Enterprise Search deployments running metricbeat as an internal monitoring component (see `monitoring.*` settings in `enterprise_search.yml`) starting with version 7.16.

### Enterprise Search Crawler

A detailed monitoring page for the Enterprise Search Crawler, showing general usage information and details on crawler activity for each node.

This dashboard should work with standalone Metricbeat deployments and with Enterprise Search deployments running metricbeat as an internal monitoring component (see `monitoring.*` settings in `enterprise_search.yml`) starting with version 8.0.

## Known Issues

* Dashboards for 7.16 do not support multi-node deployments (all node-specific metrics will be mixed from multiple nodes instead of being aggregated). The issue is fixed in 8.0.0 version of dashboards.

