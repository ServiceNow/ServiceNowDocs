---
title: Agent Client Collector Monitoring default checks and policies
description: Agent Client Collector Monitoring provides various default checks and policies.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 35
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Monitoring default checks and policies

Agent Client Collector Monitoring provides various default checks and policies.

## Provided checks

The following tables list the default checks. You can edit these checks as needed. For more information about a specific check, see its Check Definitions page, as described in [Checks and policies](../concept/checks-policies.md).

<table id="table_yds_5j1_ckb"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event

</td><td>

os.linux.check-process

</td><td>

Counts the number of running processes.You can block event creation for this check when no process is detected. For details, see [Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md).

</td></tr><tr><td>

Event

</td><td>

os.linux.check-system-cpu

</td><td>

Checks the CPU usage percentage.

</td></tr><tr><td>

Event

</td><td>

os.linux.check-system-cpu-load

</td><td>

Checks the CPU data load percentage against the configured thresholds.

</td></tr><tr><td>

Event

</td><td>

os.linux.metrics-system-disk-usage

</td><td>

Checks the file system's mount points and metrics.

</td></tr><tr><td>

Event

</td><td>

os.linux.check-system-memory-percentage

</td><td>

Checks the memory usage percentage.

</td></tr><tr><td>

Event

</td><td>

os.linux.check-system-memory-swap

</td><td>

Checks the memory swap usage.

</td></tr><tr><td>

Event

</td><td>

os.linux.check-threads-count

</td><td>

Counts the number of threads running on the system. Sends an alert if that number is greater than the Warning or Critical threshold values.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-memory-vmstat

</td><td>

Collects vmstat memory metrics.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-process-status

</td><td>

Collects process status metrics provided to the metrics parameter.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-cpu

</td><td>

Collects CPU metrics, including cores.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-cpu-load

</td><td>

Uses uptime to collect CPU load metrics.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-cpu-percentage

</td><td>

Collects CPU usage percentage metrics, including average CPU utilization percentage.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-disk

</td><td>

Collects disk metrics.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-disk-capacity

</td><td>

Collects disk capacity metrics.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-disk-usage

</td><td>

Collects disk usage metrics, providing total, used, and available disk memory, as well as the disk's percentage of memory used.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-memory

</td><td>

Collects memory metrics, providing data in KB.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-memory-percent

</td><td>

Collects memory percentage metrics.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-system-uptime

</td><td>

Collects system uptime in seconds.

</td></tr><tr><td>

Metric

</td><td>

os.linux.metrics-reboot-count-today

</td><td>

Collects the number of reboots performed today.

</td></tr></tbody>
</table><table id="table_jkx_mtm_pnb"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event

</td><td>

util.check-logs

</td><td>

Enables monitoring log files owned by a regular user.You can block event creation for this check when no process is detected. For details, see [Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md).

</td></tr><tr><td>

Event

</td><td>

util.check-logs-sudo

</td><td>

Enables monitoring log files owned by a root user.You can block event creation for this check when no process is detected. For details, see [Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md).

</td></tr></tbody>
</table>|Type|Name|Description|
|----|----|-----------|
|Metric|os.linux.metrics-network-interface|Retrieves all network interface related metrics for Linux servers.|
|Metric|os.linux.metrics-netstat.tcp|Retrieves metrics on TCP socket states from netstat. Useful on high-traffic web or proxy servers with large numbers of short-lived TCP connections coming and going.|

|Type|Name|Description|
|----|----|-----------|
|Event|os.windows.check-log|Enables monitoring log files on a Windows server.|

<table id="table_uqt_pk1_ckb"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event

</td><td>

os.windows.check-disk-name

</td><td>

Takes the storage drive name as input and verifies if the drive is present. Returns a CRITICAL\\WARNING\\OK value based on the parameter provided.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-event-log

</td><td>

Measures the Windows event log against parameter thresholds and returns a CRITICAL\\WARNING\\OK event.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-event-log-count

</td><td>

Measures the Windows event log against parameter thresholds and returns a CRITICAL\\WARNING\\OK event.Provides information on the number of events that have occurred within a specified duration for a single log file and a single ID. Also indicates the filters to be applied to retrieve events for a specific single-valued windows event level and provider name.

Retrieving events from multiple log files is not supported. The number of events is provided, without details of each and every event.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-event-log-details

</td><td>

Collects and filters Windows event logs based on the `duration_hour`, `event_log_level` and `log_file` values.

 Retrieves and filters Windows event logs according to the provided parameters. It returns details about the events with CRITICAL, WARNING, or OK status, based on the specified severity level.

 Supported on Windows version 7 and higher.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-env-variables

</td><td>

Checks the environmental variables using a regular expression and returns either a **WARNING** or **OK** value.If a new system variable is created after agent installation, you must restart the agent. This check can access only those user variables that are associated with the current user \(used during agent installation\).

</td></tr><tr><td>

Event

</td><td>

os.windows.check-file-hashcode-update

</td><td>

Takes the file's path and MD5 hashcode as an input and verifies whether file content has been modified. Returns a **CRITICAL**, **WARNING**, or **OK** value.Read permissions are required on the monitored file.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-file-update

</td><td>

Takes the file's path and interval as an input and verifies whether file content has been modified. Returns a **CRITICAL**, **WARNING**, or **OK** value.Read permissions are required on the monitored file.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-modules

</td><td>

Verifies whether the list of modules is present.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-processor-queue-length

</td><td>

Checks Processor Queue Length.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-system-cpu-load

</td><td>

Checks the CPU load by using the `typeperf` command.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-system-disk

</td><td>

Checks disk usage under specific parameters.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-system-memory

</td><td>

Collects RAM usage.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-system-patch

</td><td>

Verifies system patch installation. Returns either a **WARNING** or **OK** value.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-system-process

</td><td>

Checks the user's task list to find running processes.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-user-account

</td><td>

Takes the list of user names as an input and verifies whether the user account is active. Returns a **CRITICAL**, **WARNING**, or **OK** value.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-windows-directory

</td><td>

Checks if a directory exists.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-windows-pagefile

</td><td>

Collects page file usage and compares it to the Warning and Critical thresholds.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Event

</td><td>

os.windows.check-windows-process

</td><td>

Checks if a user input process is running.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Event

</td><td>

util.check-windows-service

</td><td>

Checks if a user-supplied service is running on Windows.You can block event creation for this check when no process is detected. For details, see [Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md).

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-process-status

</td><td>

Retrieves the number of running instances, the percentage of CPU utilization, and the memory usage \(in kilobytes\) of the specified Windows process.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-processor-queue

</td><td>

Collects Processor Queue Length.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-system-cpu-load

</td><td>

Collects the average CPU load per second.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-system-disk-usage

</td><td>

Collects disk usage metrics.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-system-memory-percent

</td><td>

Collects RAM usage per second, providing free physical, free virtual, total physical and total virtual memory percentage.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-system-network

</td><td>

Collects network metrics.

</td></tr><tr><td>

Metric

</td><td>

os.windows.metrics-system-uptime

</td><td>

Collects system uptime.

</td></tr><tr><td>

Metric

</td><td>

util.metrics-windows-perf-counters

</td><td>

\(No description\)

</td></tr></tbody>
</table>|Type|Name|Description|
|----|----|-----------|
|Event|app.mid.check-active|Checks if the MID Server is active, based on the occurrence of LogStatusMonitor in the MID log.|
|Events|app.mid.check-logs-mid|Checks the MID logs for errors.|
|Metric|app.mid.metrics-stats|Collects MID Server information from the log and returns metrics.|

|Type|Name|Description|
|----|----|-----------|
|Event|check-haproxy|Retrieves the HAProxy load balancer details to determine whether it is running.|
|Metric|metrics-check-haproxy|Retrieves the HAProxy load balancer metrics to determine whether it is running.|

|Type|Name|Description|
|----|----|-----------|
|Event|util.check-http-response|Takes a URL or a combination of host/path/port/ssl, and checks for a 200 response that matches a pattern, if provided. Can use client certificates.|
|Event|util.check-http-follow-redirect|Checks that the URL doesn't exceed the maximum number of redirects.|
|Metric|util.metrics-http-curl|Retrieves HTTP endpoint metrics using curl.|

|Type|Name|Description|
|----|----|-----------|
|Event|util.check-http-response-code|Raises a critical event if the URL response code does not match the regex.|

<table id="table_lbg_crf_1tb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

metrics.windows.active-directory

</td><td>

Collects Active Directory metrics on the Windows host.Usage: winchecks metric-windows-active-dir -s hostname

</td><td>

`winchecks metric-windows-active-dir {{if .labels.params_scheme}} -S {{.labels.params_scheme}} {{end}}`

</td></tr></tbody>
</table>|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Metric|app.apache.metrics-apache|Retrieves Apache HTTP server metrics.|2.4.x|

|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Event|kafka.check-zookeeper-status|Raises a critical event if the hosted Kafka Zookeeper is down.|ZooKeeper 3.1.2|
|Event|kafka.check-topic-replicas|Raises a critical event if any topic has partitions with unknown replicas.|ZooKeeper 3.1.2|
|Event|kafka.check-topic-replication-factor|Raises a critical event if replication factor of at least one topic is above or below provided replication factor parameter.|ZooKeeper 3.1.2|
|Event|kafka.check-topic-leader|Raises a critical event if any topic has partitions with unknown leaders or unpreferred replica as leader.|ZooKeeper 3.1.2|
|Events|kafka.check-topic-partitions|Raises a critical event if the number of partitions for a topic is less the min\_partitions param.|ZooKeeper 3.1.2|
|Event|kafka.check-broker-status|Raises a critical event if Kafka Broker on the host is down.|Kafka 0.10.1.0|
|Metric|kafka.metrics.broker|Collects Kafka Broker Metrics from the host.|Kafka 0.10.1.0|
|Metric|kafka.metrics.zookeeper|Collects Zookeeper Metrics from the host.|ZooKeeper 3.5.0-alpha|

<table id="table_snq_v3n_trb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

azure.metrics-k8s-service

</td><td>

Provides pod, nodes, and cluster level metrics from all Azure Kubernetes services in metric form.Usage: metrics-azure-k8s-service.rb

 Command example: `metrics-azure-k8s-service.rb -S {{.labels.params_subscription_id}} -r westus2`

</td><td>

`metrics-azure-k8s-service.rb -r {{.labels.params_ci_region}} {{-s {{if.labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}}`

</td></tr></tbody>
</table><table id="table_lkx_hkn_trb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

azure.metrics-vm-cpu

</td><td>

Provides CPU-related metrics of each VM instance in the Azure region.Command example: `./metrics-azure-vm.rb -S {{.labels.params_subscription_id}} -T cpu`

</td><td>

`metrics-azure-vm.rb -r {{.labels.params_ci_region}} {{if .labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}} -T {{.labels.params_type}}`

</td></tr><tr><td>

Metric

</td><td>

azure.metrics-vm-disk

</td><td>

Provides disk-related metrics of each VM instance in the Azure region.Command example: `./metrics-azure-vm.rb -S {{.labels.params_subscription_id}} -T disk`

</td><td>

`metrics-azure-vm.rb -r {{.labels.params_ci_region}} {{if .labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}} -T {{.labels.params_type}}`

</td></tr><tr><td>

Metric

</td><td>

azure.metrics-vm-memory

</td><td>

Provides memory-related metrics of each VM instance in the Azure region.Command example: `./metrics-azure-vm.rb -S {{.labels.params_subscription_id}} -T memory`

</td><td>

`metrics-azure-vm.rb -r {{.labels.params_ci_region}} {{if .labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}} -T {{.labels.params_type}}`

</td></tr><tr><td>

Metric

</td><td>

azure.metrics-vm-network

</td><td>

Provides network-related metrics of each VM instance in the Azure region.Command example: `./metrics-azure-vm.rb -S {{.labels.params_subscription_id}} -T network`

</td><td>

`metrics-azure-vm.rb -r {{.labels.params_ci_region}} {{if .labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}} -T {{.labels.params_type}}`

</td></tr><tr><td>

Metric

</td><td>

azure.metrics-vm-flows

</td><td>

Provides flows-related metrics of each VM instance in the Azure region.Command example: `./metrics-azure-vm.rb -S {{.labels.params_subscription_id}} -T flows`

</td><td>

`metrics-azure-vm.rb -r {{.labels.params_ci_region}} {{if .labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}} -T {{.labels.params_type}}`

</td></tr></tbody>
</table><table id="table_fsk_p4c_bwb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

gcp.metrics.GCE

</td><td>

Retrieves metrics from GCP for Google Compute Engine.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-requests

</td><td>

Provides http-request metrics for all applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-resources

</td><td>

Provides metrics of the resources deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-transaction-service

</td><td>

Provides metrics for all transactions on applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-deployed-apps

</td><td>

Provides metric output of the applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-deployment-lifecycle

</td><td>

Provides lifecycle metrics applications deployed on the Glassfish server.

</td></tr></tbody>
</table><table id="table_rv5_4pj_g5b"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

glassfish.metric-jvm-level

</td><td>

Retrieves JVM metrics on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-requests

</td><td>

Provides http-request metrics for all applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-server-resources

</td><td>

Provides metrics of the resources deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-transaction-service

</td><td>

Provides metrics for all transactions on applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-deployed-apps

</td><td>

Provides metric output of the applications deployed on the Glassfish server.

</td></tr><tr><td>

Metric

</td><td>

glassfish.metric-deployment-lifecycle

</td><td>

Provides lifecycle metrics applications deployed on the Glassfish server.

</td></tr></tbody>
</table><table id="table_r5k_ghz_dkb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Minimum version

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.websphere.metrics-websphere

</td><td>

Returns IBM WebSphere application server metrics.Ensure that the user running the agent has sufficient permissions to access the required files in the `IBM Websphere AS` installation directories.

</td><td>

9

</td></tr></tbody>
</table>|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Event|app.iis.check-iis-alive|Checks if IIS is running.|-|
|Event|app.iis.check-iis-current-connections|Checks the number of current connections to the IIS server and their status, depending on the input. By default, all sites are connected to the IIS server.|-|
|Metric|app.iis.metrics-iis|Returns IIS metrics.|-|

<table id="table_jbz_22z_dkb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Minimum version

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.jboss.metrics-jboss

</td><td>

Retrieves JBoss/WildFly server metrics.Ensure that the user running the agent has sufficient permissions to access the required files in the`JBoss/WildFly` installation directories.

</td><td>

16, 17

</td></tr></tbody>
</table><table id="table_hzh_s5v_3pb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Event

</td><td>

k8s.check-kube-apiserver-available

</td><td>

Checks if Kubernetes API server is up.

</td><td>

`check-kube-apiserver-available.rb {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}}`

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-nodes-ready

</td><td>

Checks whether Kubernetes nodes are in ready-to-use state.

</td><td>

`check-kube-nodes-ready.rb {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}}`

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-pods-pending

</td><td>

Measures the threshold by which pods are in the Pending state. Determine the threshold by setting the **pending\_timeout** check parameter value \(default = 300 seconds\).

</td><td>

`check-kube-pods-pending.rb {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}}`

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-pods-restarting

</td><td>

Checks the pods that are restarting. Determine the threshold by setting the check parameter value \(default = 10\).

</td><td>

`check-kube-pods-restarting.rb {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}} {{if .labels.params_restart}} -r {{.labels.params_restart}} {{end}}`

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-pods-running

</td><td>

Checks the pods that are in the running state. Configure the threshold in the **not\_ready\_time** check parameter, in seconds \(default = 0\).

</td><td>

`check-kube-pods-running.rb {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}} {{if .labels.params_not_ready_time}} -time {{.labels.params_not_ready_time}} {{end}}`

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-pods-runtime

</td><td>

Checks whether pods are running longer than expected. Configure threshold in the check parameter \(in seconds\). You can configure both WARNING and CRITICAL thresholds.

</td><td>

check-kube-pods-runtime.rb \{\{if .labels.params\_critical\}\} -c \{\{.labels.params\_critical\}\} \{\{end\}\} \{\{if .labels.params\_warning\}\} -w \{\{.labels.params\_warning\}\} \{\{end\}\} \{\{if .labels.params\_api\_server\}\} -s \{\{.labels.params\_api\_server\}\} \{\{end\}\}

</td></tr><tr><td>

Event

</td><td>

k8s.check-kube-service-available

</td><td>

Checks whether Kubernetes services are up and running. Add the list of services to be monitored in the services' **check\_param** field as comma-separated values \(without spaces\).If you enter services that are not valid, the check fails.

</td><td>

`check-kube-pods-runtime.rb {{if .labels.params_critical}} -c {{.labels.params_critical}} {{end}} {{if .labels.params_warning}} -w {{.labels.params_warning}} {{end}} {{if .labels.params_api_server}} -s {{.labels.params_api_server}} {{end}}`

</td></tr><tr><td>

Metric

</td><td>

k8s.metrics-pods

</td><td>

Provides a pod count from all of the exposed services.

</td><td>

`metrics-pods.rb {{if .labels.params_api_server}} -s {{.labels.params__api_server }} {{end}}`

</td></tr></tbody>
</table>|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Metric|app.msssql.metrics-mssql|Retrieves MSSQL database metrics.|2016|
|Metric|app.metrics-mssql-query|Generic MSSQL query class which accepts a query and dumps metrics.|2016|

<table id="table_h2y_jbz_dkb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Minimum version

</th></tr></thead><tbody><tr><td>

Event

</td><td>

app.mysql.check-mysql-alive

</td><td>

Checks if the MySQL database is running.

</td><td>

5.7, 8

</td></tr><tr><td>

Event

</td><td>

app.mysql.check-mysql-threads

</td><td>

Checks the number of running threads on the MySQL database. Depending on the input, it determines the status: OK, Warning, or Critical.

</td><td>

5.7, 8

</td></tr><tr><td>

Event

</td><td>

util.check-mysql-query

</td><td>

Checks the length of a MySQL query result set.Ensure that you use the native\_password authentication method on the MySQL server when utilizing this check.

</td><td>

5.7, 8

</td></tr><tr><td>

Metric

</td><td>

app.mysql.metrics-mysql

</td><td>

Returns MySQL database metrics.

</td><td>

5.7, 8

</td></tr><tr><td>

Metric

</td><td>

app.mysql.metrics-mysql-processes

</td><td>

Returns MySQL database process metrics.

</td><td>

5.7, 8

</td></tr><tr><td>

Metric

</td><td>

util.metrics-mysql-query

</td><td>

Creates a formatted metric for the length of a MySQL query result set.

</td><td>

5.7, 8

</td></tr></tbody>
</table>|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Event|app.mongodb.check-mongodb-alive|Monitors whether the MongoDB server is alive and creating alerts for the MongoDB server health status.| |
|Event|app.mongodb.check-mongodb-metrics|Creates alerts for any of the MongoDB metrics, based on the threshold limit.| |
|Metric|app.mongodb.metrics-mongodb|Returns metrics of the MongoDB server and all databases.| |

|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Event|app.oracle.check-oracle-alive|Checks if the Oracle database is running.|12c, 18c|
|Metric|app.oracle.metrics-oracle|Returns Oracle database metrics.|12c, 18c|
|Metric|util.metrics-oracle-query|Generic Oracle query class that accepts a query and dumps metrics.|12c, 18c|

<table id="table_wjj_pcz_dkb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Minimum version

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.weblogic.metrics-weblogic

</td><td>

Returns Oracle WebLogic application server metrics.Ensure that the user running the agent has sufficient permissions to access the required files in the `WebLogic` installation directories.

</td><td>

12cR2

</td></tr></tbody>
</table>|Type|Event/Metric|Description|Minimum version|
|----|------------|-----------|---------------|
|Metric|app.tomcat.metrics-tomcat|Returns Apache Tomcat server metrics.|8.5.27, 9.x|

|Type|Name|Description|
|----|----|-----------|
|Event|util.check-snmp|SNMP check that compares the metric value to the default. Requires input such as server, port, SNMP community, and limits.|
|Metric|util.metrics-snmp|Collects metrics from an SNMP OID value.|
|Metric|util.metrics-snmp-bulk-sn|Collects metrics from an SNMP Table OID and returns the result as a table.|

|Type|Event/Metric|Description|Command|
|----|------------|-----------|-------|
|Metric \(Windows\)|os.windows.metrics-service-status|Collects Windows service status, providing metric of number of services running.|`winchecks metric-windows-service-status -S Wcmsvc --scheme hostname.proc`|

|Type|Name|Description|
|----|----|-----------|
|Metric|app.varnish.metrics-varnish|Collects Varnish metrics from the host.|

|Type|Name|Description|
|----|----|-----------|
|Metric|vsphere.metric-VirtualMachine|Retrieves metrics for the vSphere Virtual Machine.|
|Metric|vsphere.metric-Datastore|Retrieves metrics for the vSphere Datastore.|
|Metric|vsphere.metric-Datacenter|Retrieves metrics for the vSphere Datacenter.|
|Metric|vsphere.metric-ESX\_Server|Retrieves metrics for the vSphere ESX Server or HostSystem|

|Type|Name|Description|
|----|----|-----------|
|Metric|zscaler-monitoring-check|Verifies whether the Zscaler app is running properly.|
|Metric|zscaler-remediation-check|Shuts down and restarts the Zscaler app, and creates an incident. Runs only when the zscaler-monitoring-check fails.|

<table id="table_wfb_gkh_twb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

os.windows.metrics-system-cpu

</td><td>

Collects CPU core metrics.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks metric-windows-cpu --scheme hostname.proc`

</td></tr></tbody>
</table>|Event/Metric|Description|Command|
|------------|-----------|-------|
|os.linux.check-disk-ioTimeWeighted|Measures the `disk ioTimeWeighted` value, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-ioTimeWeighted.rb`|
|os.linux.check-disk-sectorsWritten|Measures the total number of sectors written successfully, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-sectorsWritten.rb`|
|os.linux.check-disk-sectorsRead|Measures the disk's total number of sectors read successfully, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-sectorsRead.rb`|
|os.linux.check-disk-readTime|Measures the total number of milliseconds spent by all read-against thresholds, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-readTime.rb`|
|os.linux.check-disk-writes|Measures the total number of writes completed successfully, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-writes.rb`|
|os.linux.check-disk-reads|Measures the total number of reads completed successfully, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-reads.rb`|
|os.linux.check-disk-writesMerged|Measures the `disk writesMerged` value, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-writesMerged.rb`|
|os.linux.check-disk-readsMerged|Measures the `disk readsMerged` value, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-readsMerged.rb`|
|os.linux.check-disk-writeTime|Measures the total number of milliseconds spent by all write operations, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-writeTime.rb`|
|os.linux.check-disk-ioInProgress|Measures the `disk ioInProgress` value, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-ioInProgress.rb`|
|os.linux.check-disk-iotime|Measures the `disk ioTime` value, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.|`check-disk-ioTime.rb`|

<table id="table_xsr_1zg_twb"><thead><tr><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

os.windows.check-disk-AvgSecWrite

</td><td>

Measures average disk writes per second, returning a **CRITICAL\\WARNING\\OK** message, according to the specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-AvgDisksec-write -w 1 -c 0`

</td></tr><tr><td>

os.windows.check-disk-ReadBytes-sec

</td><td>

Measures the `disk ReadBytes` value per second, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-DiskReadBytes-sec -w 1 -c 0`

</td></tr><tr><td>

os.windows.check-disk-WriteBytes-sec

</td><td>

Measures the `disk WriteBytes` value per second, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-DiskWriteBytes-sec -w 1 -c 0`

</td></tr><tr><td>

os.windows.check-disk-AvgSecRead

</td><td>

Measures the average disk reads per second, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-AvgDisksec-read -w 1 -c 0`

</td></tr></tbody>
</table><table id="table_ksf_ndh_twb"><thead><tr><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

os.windows.metrics-system-disk

</td><td>

Collects the following disk metrics:-   AvgDiskSecPerRead
-   AvgDiskSecPerWrite
-   DiskReadBytesPerSec
-   DiskWriteBytesPerSec

If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks metric-windows-disk`

</td></tr></tbody>
</table><table id="table_gz4_f2h_twb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Event \(Linux\)

</td><td>

os.linux.check-free-physical-memory

</td><td>

Measures the free physical memory percentage of the Linux system, returning a **CRITICAL\\WARNING\\OK** event message, according to the thresholds specified in the parameters.

</td><td>

`check-free-physical-memory -w 10 -c 5`

</td></tr><tr><td>

Event \(Linux\)

</td><td>

os.linux.check-free-virtual-memory

</td><td>

Measures the free virtual memory percentage of the Linux system, returning a **CRITICAL\\WARNING\\OK** event message, according to the thresholds specified in the parameters.

</td><td>

`check-free-virtual-memory -w 10 -c 5`

</td></tr><tr><td>

Event \(Windows\)

</td><td>

os.windows.check-free-physical-memory

</td><td>

Measures the free physical memory percentage of the Windows system, returning a **CRITICAL\\WARNING\\OK** event message, according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-free-physfical-memory -w 10 -c 5`

</td></tr><tr><td>

Event \(Windows\)

</td><td>

os.windows.check-free-virtual-memory

</td><td>

Measures the free virtual memory percentage of the Windows system, returning a **CRITICAL\\WARNING\\OK** event message, according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-free-physical-memory -w 10 -c 5`

</td></tr><tr><td>

Metric \(Windows\)

</td><td>

os.windows.metrics-system-memory

</td><td>

Collects the following memory metrics:-   FreePhysicalMemory
-   TotalPhysicalMemory
-   FreeVirtualMemory
-   TotalVirtualMemorySize
-   AvailableMemory
-   TotalVisibleMemorySize

</td><td>

`winchecks metric-windows-memory --scheme hostname.proc`

</td></tr></tbody>
</table><table id="table_u4h_1lh_twb"><thead><tr><th>

Type

</th><th>

Event/Metric

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Event \(Linux\)

</td><td>

os.linux.check-process-cpu

</td><td>

Measures the Linux process CPU usage, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.

</td><td>

`check-process-cpu.rb -p acc -c 95 -w 85`

</td></tr><tr><td>

Event \(Linux\)

</td><td>

os.linux.check-process-memory

</td><td>

Measures the Linux process memory usage, returning a **CRITICAL\\WARNING\\OK** message, according to the thresholds specified in the parameters.

</td><td>

`check-process-memory.rb -p acc -c 95 -w 85`

</td></tr><tr><td>

Metric \(Linux\)

</td><td>

os.linux.metrics-process-usage

</td><td>

Collects the Linux process status, including the CPU and memory data used by the process.

</td><td>

`metrics-process-usage.rb -p acc -s hostname.proc`

</td></tr><tr><td>

Event \(Windows\)

</td><td>

os.windows.check-process-cpu

</td><td>

Measures the Windows process CPU usage, returning a **CRITICAL\\WARNING\\OK** message according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-process-cpu-p acc -c 95 -w 85`

</td></tr><tr><td>

Event \(Windows\)

</td><td>

os.windows.check-process-memory

</td><td>

Measures the Windows process memory usage, returning a **CRITICAL\\WARNING\\OK** message according to the thresholds specified in the parameters.If the Windows server in use does not support Windows Management Instrumentation Command-line \(WMIC\), this check does not run.

</td><td>

`winchecks check-windows-process-memory-p acc -c 95 -w 85`

</td></tr><tr><td>

Metric \(Windows\)

</td><td>

os.windows.metrics-process-usage

</td><td>

Collects the Windows process status, including the CPU and memory data used by the process.

</td><td>

`winchecks metric-windows-process-status -n Svchost -s hostname.proc`

</td></tr></tbody>
</table>## Supported Agent policies

This table lists the supported Agent Client Collector for Monitoring policies that the check definitions are associated with. The policies consist of the monitored CIs and the checks that run on them.

<table id="table_gft_tt1_ckb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Checks

</th></tr></thead><tbody><tr><td>

Apache Events

</td><td>

Monitors operational Apache HTTP web servers.To enable monitoring if the process is alive, activate the relevant check:

-   For Linux: os.linux.check-process
-   For Windows: os.windows.check-windows-process

On the **Credentials** tab, specify Basic Auth Credentials.

</td><td>

-   os.linux.check-process
-   os.windows.check-windows-process

</td></tr><tr><td>

Apache Metrics

</td><td>

Monitors operational Apache HTTP web servers.On the **Credentials** tab, specify Basic Auth Credentials.

</td><td>

app.apache.metrics-apache

</td></tr><tr><td>

Apache Kafka Events

</td><td>

Monitors the status of Kafka Broker, Kafka topics, partictions, replicas and Zookeeper.

</td><td>

 

</td></tr><tr><td>

Apache Kafka Metrics

</td><td>

Monitors and collects metrics from Kafka Broker and Kafka Zookeeper.

</td><td>

 

</td></tr><tr><td>

Azure DB Metrics

</td><td>

Monitors Azure databases on an Azure datacenter.To enable the policy's checks:

 -   Configure a proxy agent.
-   Add the following Azure service principal credentials:
    -   Tenant ID
    -   Client ID
    -   Secret Key
-   Configure the Authentication Method as **Client secret**.
-   Add Azure credentials in the policy.
-   Provide the **subscription\_id** value in each check instance.

The default monitored CI Type is cmdb\_ci\_azure\_datacenter, but the binding occurs on the Cloud Database \(cmdb\_ci\_cloud\_database\).

For details on configuring a policy, see [Create a new Agent Client Collector policy](../task/create-edit-policies.md).

</td><td>

 

</td></tr><tr><td>

Azure k8s Service Metrics

</td><td>

Monitors the Azure CI, **cmdb\_ci\_azure\_datacenter**. Binds with the Kubernetes data cluster, **cmdb\_ci\_kubernetes\_cluster**.

</td><td>

azure.metrics-k8s-service

 For details, see [Azure Health Monitoring default checks and policies](azure-checks-policies.md).

</td></tr><tr><td>

Azure VM Metrics

</td><td>

Monitors the Azure CI, **cmdb\_ci\_azure\_datacenter**. Binds with the virtual machine instance, **cmdb\_ci\_vm\_instance**.

</td><td>

-   azure.metrics-vm-cpu
-   azure.metrics-vm-disk
-   azure.metrics-vm-memory
-   azure.metrics-vm-network
-   azure.metrics-vm-flows

 For details, see [Azure Health Monitoring default checks and policies](azure-checks-policies.md).

</td></tr><tr><td>

Basic Discovery

</td><td>

Runs basic ServiceNow Discovery on all agents, every 12 hours.This check extracts basic information about the host and its running processes. The host information is used to create the corresponding host in the CMDB, while the running processes create the classified application CIs.

You need advanced OS privileges to use the Net stat command to discover ports. The command that you run depends on your OS, as follows:

-   Linux: `sudo -n netstat -antp`
-   Windows: `netstat -anop TCP`

</td><td>

check-discovery-basic

</td></tr><tr><td>

Docker Container Metrics

</td><td>

Collects performance metrics for Docker containers.

 Provide the credentials of users who are Docker user group members or have sudo rights. Provide these credentials on the **Credentials** tab of the policy form.

</td><td>

container.docker.metrics-docker

</td></tr><tr><td>

Docker Engine Metrics

</td><td>

Collects general metrics for the Docker engine. Provides the credentials of a user which is either a member of the Docker user group or has been assigned sudo rights on the **Credentials** tab.

To enable running checks through this policy, add the servicenow user to the Docker user group on the machine where the agent is running.

</td><td>

container.docker.metrics-docker-info

</td></tr><tr><td>

F5 SNMP Events

</td><td>

Example for using SNMP checks. Because the Agent doesn't run on SNMP devices, provide the following to complete this policy:

-   A Proxy Agent and credentials.
-   The host of the Proxy Agent. On the **Credentials** tab, specify the SNMP Community Credentials for connecting to the server.

</td><td>

util.check-snmp

</td></tr><tr><td>

F5 SNMP Metrics

</td><td>

Example for using SNMP metrics. Because the Agent doesn't run on SNMP devices, provide the following to complete this policy:

-   Proxy Agent and credentials.
-   The host of the Proxy Agent. On the**Credentials** tab, specify the SNMP Community Credentials for connecting to the server.

</td><td>

-   util.metrics-snmp
-   util.metrics-snmp-bulk-sn

</td></tr><tr><td>

Glassfish Metrics

</td><td>

Runs metric checks on the Glassfish server.Glassfish metrics are supported in ITOM Agent Client Collector version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

 

</td></tr><tr><td>

HAProxy Events

</td><td>

Retrieves the HAProxy load balancer details to determine whether it is running.HAProxy events are supported in ITOM Agent Client Collector version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

 

</td></tr><tr><td>

HAProxy Metrics

</td><td>

Retrieves the HAProxy load balancer metrics to determine whether it is running.HAProxy metrics are supported in ITOM Agent Client Collector version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

 

</td></tr><tr><td>

HTTP Entry Points Events

</td><td>

Runs the util.check-http-follow-redirect check on all HTTP entry points that belong to application business services. The policy filter chooses the services. The services define the entry points. -   To enable this check, there is a new database view which combines the application services table with the entry points table.
-   You can filter the services and receive the entry points.
-   When you receive an alert, it is automatically bound to the entry points. This alert affects the impact calculation, because entry points are considered.
-   This policy requires a Proxy Agent.

</td><td>

util.check-http-follow-redirect

</td></tr><tr><td>

HTTP Entry Points Metrics

</td><td>

For example, when the alert is bound to the entry point, the service map identifies an entry point problem. -   The metric binds to the entry point CI. In previous releases, the metric was bound to the service and the entry point was the resource.
-   This policy requires a Proxy Agent.

</td><td>

util.metrics-http-curl

</td></tr><tr><td>

IIS Events

</td><td>

Monitors operational IIS servers.

</td><td>

-   app.iis.check-iis-alive
-   app.iis.check-iis-current-connections

</td></tr><tr><td>

IIS Metrics

</td><td>

Monitors operational IIS servers.

</td><td>

app.iis.metrics-iis

</td></tr><tr><td>

JBoss/WildFly Application Server Events

</td><td>

Monitoring operational JBoss/WildFly application servers.To enable monitoring if the JBoss process is alive, activate os.linux.check-process.

The **jboss\_home** parameter in the check instance is specified as the location where JBoss is installed.

</td><td>

os.linux.check-process

</td></tr><tr><td>

JBoss/WildFly Application Server Metrics

</td><td>

Monitors operational JBoss/WildFly application servers.

</td><td>

app.jboss.metrics-jboss

</td></tr><tr><td>

Kubernetes

</td><td>

Monitors health of Kubernetes infrastructure, such as clusters, nodes, pod status, API, and service availability.When running Kubernetes checks:

-   Proxy agent must be enabled.
-   Enter Kubernetes credentials, either a username/password combination or a bearer token \(but not both\).
-   To activate and publish the policy, configure the **api\_server** value in the check parameter definitions of each check, as one of the following:

    -   `https://127.0.0.1:<portnumber>/api` \(If the API server and agent are running on the same server\)
    -   `https://<api_server_url>/api` \(Whether the API server and agent are running on the same or different servers\).
To use the localhost as your api\_server, run the following command: `"kubectl proxy -port=8081 &"`

-   Run Discovery to discover all Kubernetes CIs. For details, see [Kubernetes discovery](../../service-mapping/concept/kubernetes-discovery.md).

</td><td>

-   k8s.check-kube-apiserver-available
-   k8s.check-kube-nodes-ready
-   k8s.check-kube-pods-pending
-   k8s.check-kube-pods-restarting
-   k8s.check-kube-pods-running
-   k8s.check-kube-pods-runtime
-   k8s.check-kube-service-available
-   k8s.metrics-pods

</td></tr><tr><td>

Linux log monitoring

</td><td>

Monitors logs on operational Linux servers.

</td><td>

-   util.check-logs
-   util.check-logs-sudo

</td></tr><tr><td>

Linux OS Events

</td><td>

Runs Linux checks on operational Linux servers.

</td><td>

-   os.linux.check-process
-   os.linux.check-system-cpu
-   os.linux.check-system-cpu-load
-   os.linux.check-system-disk-usage
-   os.linux.check-system-memory-percentage
-   os.linux.check-system-memory-swap
-   os.linux.check-threads-count

</td></tr><tr><td>

Linux OS Metrics

</td><td>

Collects Linux metrics on operational Linux servers.

</td><td>

-   os.linux.metrics-memory-vmstat
-   os.linux.metrics-process-status
-   os.linux.metrics-system-cpu
-   os.linux.metrics-system-cpu-load
-   os.linux.metrics-system-disk
-   os.linux.metrics-system-disk-capacity
-   os.linux.metrics-system-disk-usage
-   os.linux.metrics-system-memory
-   os.linux.metrics-system-memory-percentage
-   os.linux.metrics.reboot\_count\_today

</td></tr><tr><td>

MSSQL Events

</td><td>

Monitors the operational MSSQL server process. Runs os.windows.check-windows-process to monitor when the server process is alive.

</td><td>

os.windows.check-windows-process

</td></tr><tr><td>

MSSQL Metrics

</td><td>

Monitors operational MSSQL server process. Runs app.mssql.metrics-mssql to gather metrics.

</td><td>

app.mssql.metrics-mssql

</td></tr><tr><td>

MySQL DB Events

</td><td>

Monitors operational MySQL instances.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the database server.

**Note:** Utility checks, prefixed with util, have required parameters for which you must specify a value. These parameters have no default values.

</td><td>

-   app.mysql.check-mysql-alive
-   app.mysql.check-mysql-threads
-   util.check-mysql-query

</td></tr><tr><td>

MySQL DB Metrics

</td><td>

Monitors operational MySQL instances.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the database server.

**Note:** Utility checks, prefixed with util, have required parameters for which you must specify a value. These parameters have no default values.

</td><td>

-   app.mysql.metrics-mysql
-   app.mysql.metrics-mysql-processes
-   util.metrics-mysql-query

</td></tr><tr><td>

Network ping metrics

</td><td>

Monitors the ip address discovered in the ServiceNow instance. The cmdb\_ci\_hardware monitored CI type is bound to the relevant server:This policy requires a proxy agent.

</td><td>

util.metrics-ping

</td></tr><tr><td>

Oracle DB Events

</td><td>

Monitors operational Oracle Database instances.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the database server.

**Note:** Utility checks, prefixed with util, have required parameters for which you must specify a value. These parameters have no default values.

</td><td>

app.oracle.check-oracle-alive

</td></tr><tr><td>

Oracle DB Metrics

</td><td>

Monitors operational Oracle Database instances.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the database server.

**Note:** Utility checks, prefixed with util, have required parameters for which you must specify a value. These parameters have no default values.

</td><td>

-   app.oracle.metrics-oracle
-   util.metrics-oracle-query

</td></tr><tr><td>

Self-Healing Events

</td><td>

Runs a ping command to another host. Ensure that you run this check in proxy mode.

</td><td>

util.check-ping

</td></tr><tr><td>

Tomcat Events

</td><td>

Monitors operational Apache Tomcat servers. To enable monitoring if the Tomcat process is alive, activate the relevant check:

-   For Linux: os.linux.check-process
-   For Windows: util.check-windows-service

 If the Tomcat service is running under a different name, update the value of the check instance's **service** parameter to the correct value.

</td><td>

-   os.linux.check-process
-   util.check-windows-service

</td></tr><tr><td>

Tomcat Metrics

</td><td>

Monitors operational Apache Tomcat servers.If Tomcat Metrics are running on a port other than the default port \(9000\), update the value of the check instance's **port** parameter to the correct port value.

</td><td>

app.tomcat.metrics-tomcat

</td></tr><tr><td>

Varnish Metrics

</td><td>

Monitors and collects metrics from Varnish.Varnish metrics are supported in ITOM Agent Client Collector version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

 You must perform discovery using application fingerprints before running Varnish checks. For details, see [Enable running of Varnish checks](../task/discover-varnish-ci.md).

</td><td>

 

</td></tr><tr><td>

vSphere Metrics

</td><td>

Monitors and collects metrics from vSphere.vSphere metrics are supported in ITOM Agent Client Collector version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

This policy requires a proxy agent.

</td><td>

 

</td></tr><tr><td>

WebLogic Application Server Events

</td><td>

Monitors operational Oracle WebLogic application servers. This policy monitors if the WebLogic process running on Linux is alive.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the application server.

</td><td>

os.linux.check-process

</td></tr><tr><td>

WebLogic Application Server Metrics

</td><td>

Monitors operational Oracle WebLogic application servers.On the **Credentials** tab, specify Basic Auth Credentials for connecting to the application server.

 Ensure that the user running the agent has sufficient permissions to access the required files in the `WebLogic` installation directories.

</td><td>

app.weblogic.metrics-weblogic

</td></tr><tr><td>

WebSphere Application Server Events

</td><td>

Monitors operational IBM WebSphere servers. This policy monitors if the WebSphere process running on Linux is alive. On the **Credentials** tab, specify Basic Auth Credentials for connecting to the application server.

</td><td>

os.linux.check-process

</td></tr><tr><td>

WebSphere Application Server Metrics

</td><td>

Monitors operational IBM WebSphere servers. On the **Credentials** tab, specify Basic Auth Credentials for connecting to the application server.

</td><td>

app.websphere.metrics-websphere

</td></tr><tr><td>

Windows Log Monitoring

</td><td>

Monitors logs on operational Windows servers.

</td><td>

os.windows.check-log

 You can block event creation for this check when no process is detected. For details, see [Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md).

</td></tr><tr><td>

Windows OS Events

</td><td>

Runs Windows checks on operational Windows servers.

</td><td>

-   os.windows.check-processor-queue-length
-   os.windows.check-system-cpu-load
-   os.windows.check-system-disk
-   os.windows.check-system-memory
-   os.windows.check-system-process
-   os.windows.check-windows-directory
-   os.windows.check-windows-directory
-   os.windows.check-windows-directory
-   os.windows.check-windows-pagefile
-   os.windows.check-windows-process

</td></tr><tr><td>

Windows OS Events - Extended

</td><td>

Runs Windows checks to monitor directories and files on Windows servers.

</td><td>

-   check-directory-file-count
-   check-directory-integrity
-   check-file-age
-   check-file-response-time
-   check-file-size
-   check-file-space
-   os.windows.check-directory-space

</td></tr><tr><td>

Windows OS Metrics

</td><td>

Collects Windows metrics on operational Windows servers.

</td><td>

-   os.windows.metrics-processor-queue-len
-   os.windows.metrics-system-cpu-load
-   os.windows.metrics-system-disk-usage
-   os.windows.metrics-system-memory-percent
-   os.windows.metrics-system-network
-   os.windows.metrics-system-uptime

</td></tr><tr><td>

Zscaler Monitoring Policy

</td><td>

Executes Zscaler monitoring on all of a machine's CIs.

</td><td>

-   zscaler-monitoring-check
-   zscaler-remediation-check

</td></tr></tbody>
</table>-   **[Active Directory metrics](ad-metrics.md)**  
The following table lists the metrics that are gathered as output from Active Directory checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Apache Kafka default checks and policies](kafka-checks-policies.md)**  
Agent Client Collector provides the following policies for Apache Kafka health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
-   **[Apache Kafka metrics](kafka-metrics.md)**  
The following table lists the metrics that are gathered as output from Kafka checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[AWS Health Monitoring default checks and policies](aws-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for AWS monitoring.
-   **[AWS metrics](aws-metrics.md)**  
The following tables list and describe the metrics that are gathered as output from the specified AWS checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Azure Health Monitoring default checks and policies](azure-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for Azure health monitoring.
-   **[Azure metrics](azure-metrics.md)**  
The following tables list and describe the metrics that are gathered as output from Azure checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Azure cloud metrics](../concept/azure-cloud-metrics.md)**  
Azure cloud metrics are gathered from Azure virtual machines \(VMs\) and Azure storage account policies. Collecting the cloud metrics enables you to monitor the performance of your Azure resources.
-   **[Cassandra default checks and policies](cassandra-checks-policies.md)**  
Agent Client Collector provides the following policies for Cassandra health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for Linux only.
-   **[Cassandra metrics](cassandra-metrics.md)**  
The following table lists the metrics that are gathered as output from Cassandra checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Directory Scan monitoring default checks and policies](directory-scan-checks-policies.md)**  
The Agent Client Collector provides the following default checks and policies for Directory Scan monitoring.
-   **[Glassfish default checks and policies](glassfish-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for Glassfish monitoring.
-   **[GlassFish metrics](glassfish-metrics.md)**  
The following table lists the metrics that are gathered as output from GlassFish checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[HAProxy default checks and policies](haproxy-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for HAProxy monitoring.
-   **[HAProxy metrics](haproxy-metrics.md)**  
The following table lists the metrics that are gathered as output from HAProxy checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[HTTP default checks and policies](http-default-checks-policies.md)**  
Agent Client Collector provides the following policies for HTTP health monitoring. Policies come with the checks specified in the tables below.
-   **[HTTP entry point metrics](httpentrypoint-metrics.md)**  
The following table lists the metrics that are gathered as output from HTTP entry point checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[HTTP response code check](http-response-code-check.md)**  
Agent Client Collector provides the following additional check for HTTP response code. This check is not associated with any policy.
-   **[Internet Information Services \(IIS\) metrics](iis-metrics.md)**  
The following table lists the metrics that are gathered as output from IIS checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Linux default checks and policies](linux-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for Linux Metrics monitoring.
-   **[Linux metrics](linux-metrics.md)**  
The following table lists the metrics that are gathered as output from Linux checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[MongoDB default checks and policies](mongodb-checks-policies.md)**  
Agent Client Collector provides the following policies for MongoDB health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
-   **[MongoDB metrics](mongodb-metrics.md)**  
The following table lists the metrics that are gathered as output from MongoDB checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[MS Exchange default checks and policies](msexchange-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for MS Exchange monitoring.
-   **[MSSQL default checks and policies](ms-sql-default-checks-and-policies.md)**  
The Agent Client Collector provides the following default checks and policies for MSSQL Metrics monitoring.
-   **[MySQL default checks and policies](my-sql-default-checks-and-policies.md)**  
The Agent Client Collector provides the following default checks and policies for MySQL Metrics monitoring.
-   **[Network ping default checks and policies](network-ping-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for Network ping monitoring. Policies and checks are available for both Windows and Linux.
-   **[Network ping metrics](network-ping-metrics.md)**  
The following table lists the metrics that are gathered as output from Network ping checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Network host availability check](network-host-availability-check.md)**  
Agent Client Collector provides the following default check for network ping monitoring. The check is available for both Windows and Linux.
-   **[Nginx default checks and policies](nginx-checks-policies.md)**  
Agent Client Collector provides the following policies for Nginx health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
-   **[Nginx metrics](nginx-metrics.md)**  
The following table lists the metrics that are gathered as output from Nginx checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[PostgreSQL default checks and policies](postgresql-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for PostgreSQL health monitoring.
-   **[PostgreSQL metrics](postgresql-metrics.md)**  
The following tables list and describe the metrics that are gathered as output from the specified PostgreSQL checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[RabbitMQ default checks and policies](rabbitmq-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for RabbitMQ health monitoring. You must perform RabbitMQ discovery before executing the checks. RabbitMQ checks are available only in a Windows environment.
-   **[RabbitMQ metrics](rabbitmq-metrics.md)**  
The following table lists the metrics that are gathered as output from RabbitMQ checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[URL Monitoring default checks and policies](url-monitoring-default-checks-policies.md)**  
Agent Client Collector provides policies for URL Monitoring. Polices come with embedded checks.
-   **[Varnish default checks and policies](varnish-policies-checks.md)**  
Agent Client Collector provides the following default checks and policies for Varnish monitoring.
-   **[Varnish metrics](varnish-metrics.md)**  
The following table lists the metrics that are gathered as output from Varnish checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[vSphere default checks and policies](vsphere-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for vSphere monitoring.
-   **[vSphere metrics](vsphere-metrics.md)**  
The following table lists the metrics that are gathered as output from vSphere checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Windows default checks and policies](windows-checks-policies.md)**  
Agent Client Collector provides the following default checks and policies for Windows health monitoring.
-   **[Windows metrics](windows-metrics.md)**  
The following table lists the metrics that are gathered as output from Windows checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
-   **[Windows log monitoring default checks and policies](windows-log-monitoring-policy.md)**  
Agent Client Collector provides the following policy for Windows log monitoring.
-   **[Linux log monitoring default checks and policies](linux-log-monitoring-policy.md)**  
Agent Client Collector provides the following policy for Linux log monitoring.

**Parent Topic:**[Agent Client Collector Monitoring reference](acc-monitoring-reference.md)

