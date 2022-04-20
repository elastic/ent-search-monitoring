# Elastic Enterprise Search Monitoring Dashboard

This directory contains a set of [Kibana dashboards](https://www.elastic.co/guide/en/kibana/current/dashboard.html) to be used with [Elastic Enterprise Search](https://www.elastic.co/enterprise-search) and Elastic Metricbeat for monitoring production deployments.

**Please note:** These dashboards only work with Kibana and Enterprise Search versions 7.16.0 and higher. Dashboards differ between versions of the stack, so please pick the version closest to your current release, but not higher (8.0 for any 8.x release, 7.16 for releases before 8.0).

## Installation

Dashboards are imported on the **Stack Management > Saved objects** page. Full documentation on this process is available in [Kibana](https://www.elastic.co/guide/en/kibana/current/managing-saved-objects.html).

After importing, visit the [Dashboard](https://www.elastic.co/guide/en/kibana/current/dashboard.html) tab to view and edit your imported dashboards.

For more information on Enterprise Search monitoring, please refer to [Enterprise Search documentation](https://www.elastic.co/guide/en/enterprise-search/current/index.html).

## Dashboards

The following dashboard is available at this time:

### Enterprise Search Overview

This dashboard provides a general monitoring overview page with product usage information, HTTP metrics, low-level resource utilization information (JVM metrics) and background workers details.

This dashboard works with Enterprise Search (both on premise and Cloud deployments), as well as with standalone Metricbeat deployments for Enterprise Search. See `monitoring.*` settings in `enterprise_search.yml` starting with version 7.16.
