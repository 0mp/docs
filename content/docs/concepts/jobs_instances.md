---
title: Jobs and instances
sort_rank: 3
---

# Jobs and instances

In Prometheus terms, any individually scraped target is called an _instance_,
usually corresponding to a single process. A collection of instances of the
same type (replicated for scalability or reliability) is called a _job_.

For example, an API server job with four replicated instances:

   * job: `api-server`
      * instance 1: `1.2.3.4:5670`
      * instance 2: `1.2.3.4:5671`
      * instance 3: `5.6.7.8:5670`
      * instance 4: `5.6.7.8:5671`

## Automatically generated labels and time series

When Prometheus scrapes a target, it attaches some labels automatically to the
scraped time series which serve to identify the scraped target:

* `job`: The configured job name that the target belongs to.
* `instance`: The `<host>:<port>` part of the target's URL that was scraped.

If either of these labels are already present in the scraped data, the behavior
depends on the `honor_labels` configuration option. See the
[scrape configuration documentation](/docs/operating/configuration/#scrape-configurations-scrape_config)
for more information.

For each instance scrape, Prometheus stores a sample of the form
`up{job="<job-name>", instance="<instance-id>"}` with a value of `1` if the
instance was scraped successfully or a value of `0` if the scrape failed. This
time series is useful for instance availability monitoring.
