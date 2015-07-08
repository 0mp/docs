---
title: Exporters and third-party integrations
sort_rank: 3
---

# Exporters and third-party integrations

There are a number of libraries and servers which help in exporting existing
metrics from third-party systems as Prometheus metrics. This is useful for
cases where it is not feasible to instrument a given system with Prometheus
metrics directly (for example, HAProxy or Linux system stats).

## Official third-party exporters

These exporters are maintained as part of the official
[Prometheus GitHub organization](https://github.com/prometheus):

   * [Node/system metrics exporter](https://github.com/prometheus/node_exporter)
   * [AWS CloudWatch exporter](https://github.com/prometheus/cloudwatch_exporter)
   * [Collectd exporter](https://github.com/prometheus/collectd_exporter)
   * [Consul exporter](https://github.com/prometheus/consul_exporter)
   * [Graphite exporter](https://github.com/prometheus/graphite_exporter)
   * [HAProxy exporter](https://github.com/prometheus/haproxy_exporter)
   * [Hystrix metrics publisher](https://github.com/prometheus/hystrix)
   * [JMX exporter](https://github.com/prometheus/jmx_exporter)
   * [Mesos task exporter](https://github.com/prometheus/mesos_exporter)
   * [MySQL server exporter](https://github.com/prometheus/mysqld_exporter)
   * [StatsD bridge](https://github.com/prometheus/statsd_bridge)

The [JMX exporter](https://github.com/prometheus/jmx_exporter) can export from a
wide variety of JVM-based applications, for example [Kafka](http://kafka.apache.org/) and
[Cassandra](http://cassandra.apache.org/).

## Independently maintained third-party exporters

There are also a number of exporters which are externally contributed
and maintained. We encourage the creation of more exporters but cannot
vet all of them for best practices. Commonly, those exporters are
hosted outside of the Prometheus GitHub organization.

   * [CouchDB exporter](https://github.com/gesellix/couchdb-exporter)
   * [Django exporter](https://github.com/korfuri/django-prometheus)
   * [Google's mtail log data extractor](https://github.com/google/mtail)
   * [Memcached exporter](https://github.com/Snapbug/memcache_exporter)
   * [Meteor JS web framework exporter](https://atmospherejs.com/sevki/prometheus-exporter)
   * [Minecraft exporter module](https://github.com/Baughn/PrometheusIntegration)
   * [MongoDB exporter](https://github.com/dcu/mongodb_exporter)
   * [Munin exporter](https://github.com/pvdh/munin_exporter)
   * [New Relic exporter](https://github.com/jfindley/newrelic_exporter)
   * [RabbitMQ exporter](https://github.com/kbudde/rabbitmq_exporter)
   * [Redis exporter](https://github.com/oliver006/redis_exporter)
   * [RethinkDB exporter](https://github.com/oliver006/rethinkdb_exporter)
   * [scollector exporter](https://github.com/tgulacsi/prometheus_scollector)
   * [Rsyslog exporter](https://github.com/digitalocean/rsyslog_exporter)

## Directly instrumentated software

Some third-party software already exposes Prometheus metrics natively, so no
separate exporters are needed:

   * [cAdvisor](https://github.com/google/cadvisor)
   * [Etcd](https://github.com/coreos/etcd)
   * [go-metrics instrumentation library](https://github.com/armon/go-metrics)
   * [gokit](https://github.com/peterbourgon/gokit)
   * [Kubernetes-Mesos](https://github.com/mesosphere/kubernetes-mesos)
   * [Kubernetes](https://github.com/GoogleCloudPlatform/kubernetes)
   * [RobustIRC](http://robustirc.net/)
