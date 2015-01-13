---
title: Exporters for third-party systems
sort_rank: 3
---

# Exporters for third-party systems

There are a number of libraries and servers which help in exporting existing
metrics from third-party systems as Prometheus metrics. This is useful for
cases where it is not feasible to instrument a given system with Prometheus
metrics directly (for example, HAProxy or Linux system stats). The
following is a list of existing third-party exporters:

   * [Node/system metrics exporter](https://github.com/prometheus/node_exporter)
   * [HAProxy exporter](https://github.com/prometheus/haproxy_exporter)
   * [AWS CloudWatch exporter](https://github.com/prometheus/cloudwatch_exporter)
   * [StatsD bridge](https://github.com/prometheus/statsd_bridge)
   * [JMX exporter](https://github.com/prometheus/jmx_exporter)
   * [Hystrix metrics publisher](https://github.com/prometheus/hystrix)
