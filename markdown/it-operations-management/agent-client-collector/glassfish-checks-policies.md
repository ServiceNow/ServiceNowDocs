---
title: Glassfish default checks and policies
description: Agent Client Collector provides the following default checks and policies for Glassfish monitoring.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Glassfish default checks and policies

Agent Client Collector provides the following default checks and policies for Glassfish monitoring.

<table id="table_a3f_qsc_g5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and usage example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

glassfish.metric-jvm-level

</td><td>

Retrieves the Glassfish server's JVM metrics.

 Requires basic authentication credentials.

</td><td>

```
-i, --instance  Glassfish Monitoring Instance Name (required)
-p, --password  Glassfish password
-P, --port  Glassfish API port
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username

```

 Usage example: `metric-glassfish-jvm-level.rb {{if .labels.params_port}} -P {{.labels.params_port}} {{end}} -i {{.labels.params_glassfish_server_instance}}`

</td><td>

`glassfish.jvm.garbage-collectors.Scavenge.CollectionCount 200 0 1652959788`

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-requests

</td><td>

Provides http-request metrics for all applications deployed on the Glassfish server.

 Requires basic authentication credentials.

</td><td>

```
-i, --instance  Glassfish Monitoring Instance Name (required)
-p, --password  Glassfish password
-P, --port  Glassfish API port
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username

```

 Usage example: `metric-glassfish-server-requests.rb -i {{.labels.params_glassfish_server_instance}} {{if .labels.params_port}} -P {{.labels.params_port}} {{end}}`

</td><td>

`glassfish.http-service.server.request.Count 200 0 1652959788`

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-resources

</td><td>

Provides metrics of the resources deployed on the Glassfish server.

 Requires basic authentication credentials.

</td><td>

```
-i, --instance  Glassfish Monitoring Instance Name (required)
-P, --port  Glassfish API port
-r --resource_pool  Resource Pool Name
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username
-p --password  Glassfish password

```

 Usage example: `metric-glassfish-server-resources.rb {{if .labels.params_port}} -P {{.labels.params_port}} {{end}} {{if .labels.params_resource_pool}} -r {{.labels.params_resource_pool}} {{end}} -i {{.labels.params_glassfish_server_instance}}`

</td><td>

`glassfish.resources.{{PoolName}}.AverageConnWaitTime 0 1652959936`

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-transaction-service

</td><td>

Provides metrics for all transactions on applications deployed on the Glassfish server.

 Requires basic authentication credentials.

</td><td>

```
-i, --instance  Glassfish Monitoring Instance Name (required)
-P, --port  Glassfish API port
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username
-p --password  Glassfish password

```

 Usage example: `metric-glassfish-transaction-service.rb {{if .labels.params_port}} -P {{.labels.params_port}} {{end}} -i {{.labels.params_glassfish_server_instance}}`

</td><td>

`glassfish.transaction-service.ActiveCount 0 1652959977`

</td></tr><tr><td>

Metric

</td><td>

glassfish.metrics-deployed-apps

</td><td>

Provides metric output of applications deployed on the Glassfish server.

 Requires basic authentication credentials.

</td><td>

```
-a, --apps  Application deployed on Glassfish server (required)
-i, --instance  Glassfish Monitoring Instance Name (required)
-P, --port  Glassfish API port
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username
-p --password  Glassfish password

```

 Usage example: `metric-glassfish-deployed-applications.rb {{if .labels.params_port}} -P {{.labels.params_port}} {{end}} -a {{.labels.params_deployed_apps}} -i {{.labels.params_glassfish_server_instance}}`

</td><td>

`glassfish.applications.{{Deployed Application}}.ActivatedSessionsTotal 0 1652959665`

</td></tr><tr><td>

Metric

</td><td>

glassfish.metrics-deployment-lifecycle

</td><td>

Provides lifecycle metrics of the Glassfish server applications.

 Requires basic authentication credentials.

</td><td>

```
metric-glassfish-deployment-lifecycle.rb (options)
-i, --instance  Glassfish Monitoring Instance Name (required)
-p --password  Glassfish password
-P, --port  Glassfish API port
--ssl  Enable secure connnection to Glassfish
-u –username  Glassfish username

```

 Usage example: `metric-glassfish-deployment-lifecycle.rb {{if .labels.params_port}} -P {{.labels.params_port}} {{end}} -i {{.labels.params_glassfish_server_instance}}`

</td><td>

`glassfish.deployment.lifecycle.ActiveApplicationsDeployed 2 1653022649`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

