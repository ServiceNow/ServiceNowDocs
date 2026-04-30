---
title: Apache Kafka default checks and policies
description: Agent Client Collector provides the following policies for Apache Kafka health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Apache Kafka default checks and policies

Agent Client Collector provides the following policies for Apache Kafka health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.

<table id="table_y3r_2qd_2tb"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

kafka.check-zookeeper-status

</td><td>

Raises a critical event if the hosted Kafka Zookeeper is down.

</td><td>

`commonchecks check-kafka-zk-status` \[flags\]Where the flags are:

 `-p, --port =` Zookeeper Port \(default "2181"\).Usage example: `commonchecks check-kafka-zk-status -p 2181`

</td><td>

Kafka Zookeeper Status OK: Kafka Zookeeper is Up!

</td></tr><tr><td>

kafka.check-topic-replicas

</td><td>

Raises critical event if any topic has partitions with unknown replicas.

</td><td>

`commonchecks check-kafka-replicas` \[flags\]Where the flags are:

 -   `-p, --port =` Zookeeper Port \(default "2181"\).
-   `-d, --detailed` = Lists unknown replicas in each partition of a topic.
-   `-i, --include_list` = Comma seperated list to include topics \(allows \* wild character\)
-   `-e, --exclude_list` = Comma seperated list to exclude topics \(allows \* wild character\)

Usage example: commonchecks check-kafka-replicas -H localhost -p 2181 -i "test\*" -e "accTopic,\*offsets" -d

</td><td>

&lt;topic&gt; has partitions with unknown replicas. Unknown replicas are: \{"0":\["0"\],"1":\["0"\],"2":\["0"\]\}.

 &lt;topic&gt; has partitions with unknown replicas. Unknown replicas are: \{"0":\["0"\]\}.

</td></tr><tr><td>

kafka.check-topic-replication-factor

</td><td>

Raises critical event if replication factor of at least one topic is above or below provided replication factor param.

</td><td>

`commonchecks check-kafka-rf` \[flags\]Where the flags are:

 -   `-p, --port =` Zookeeper Port \(default "2181"\).
-   `-d, --detailed` = Lists unknown replicas in each partition of a topic.
-   `-i, --include_list` = Comma separated list to include topics \(allows \* wild character\)
-   `-e, --exclude_list` = Comma separated list to exclude topics \(allows \* wild character\)
-   `-r, --replication factor` = Expected replication factor for a topic \(default 1\)

 Examples: `commonchecks check-kafka-partitions -H localhost -p 2181 -r 2 -i "accMetrics,*Topic" -e "testTopic"`

</td><td>

TestTopic has replication factor 1, which is less than expected: 2.

 accMetrics has replication factor 1, which is less than expected: 2.

</td></tr><tr><td>

kafka.check-topic-leader

</td><td>

Raises critical event if any topic has partitions with unknown leaders or unpreferred replica as leader.

</td><td>

`commonchecks check-kafka-leader` \[flags\]Where the flags are

 -   `-p, --port` = Zookeeper Port \(default "2181"\).
-   `-d, --detailed` = A list of partitions in each topic with unknown leaders or unpreferred replicas.
-   `-i, --include_list` = Comma separated list to include topics \(allows \* wild character\)
-   `-e, --exclude_list` =Comma separated list to exclude topics \(allows \* wild character\)

 Examples:

 `commonchecks check-kafka-leader -H localhost -p 2181 -d -e "*offsets"`

</td><td>

&lt;topic&gt; contains, partitions with unpreferred replica as leader.\(partitions with unpreferred replicas are \[0\]\).

 &lt;topic&gt; contains, partitions with unpreferred replica as leader.\(partitions with unpreferred replicas are \[0\]\).

</td></tr><tr><td rowspan="3">

kafka.check-topic-partitions

</td><td rowspan="3">

Raises critical events if number of partitions for a topic is less the min\_partitions param.

</td><td>

`commonchecks check-kafka-partitions [flags]` Where the flags are:

 -   `-p, --port` = Zookeeper Port \(default "2181"\).
-   `-P, --min_partitions` = Minimum partitions for a topic \(default 1\).
-   `-i, --include_list` = Comma separated list to include topics \(allows \* wild character\)
-   `-e, --exclude_list` =Comma separated list to exclude topics \(allows \* wild character\)

</td><td>

 

</td></tr><tr><td>

Usage example 1: `commonchecks check-kafka-partitions -H localhost -p 2181 -P 3`

</td><td>

&lt;topic&gt; has 1 partitions, expected at least 3.

 &lt;topic&gt; has 1 partitions, expected at least 3.

 &lt;topic&gt; has 1 partitions, expected at least 3.

</td></tr><tr><td>

Usage example 2: commonchecks check-kafka-partitions -H localhost -p 2181 -P 3 -i "accMetrics,\*Topic" -e "testTopic"

</td><td>

&lt;topic&gt; has 1 partitions, expected at least 3.

 &lt;topic&gt; has 1 partitions, expected at least 3.

</td></tr></tbody>
</table>**Note:** Values for include\_list and exclude\_list parameters have to be wrapped between double quotes. For example: "test1,\*topic".

<table id="table_hxk_5dm_f5b"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

kafka.check-broker-status

</td><td>

Raises critical event if Kafka Broker on the host is down.

</td><td>

`commonchecks check-kafka-broker-status` \[flags\]Where the flags are:

 `-p, --port` = Kafka Broker port \(default "9092"\).Usage example: `commonchecks check-kafka-broker-status -p 9092`

</td><td>

Kafka Broker Status OK: Kafka Broker ubuntu20:9092 is Up!

</td></tr></tbody>
</table><table id="table_emg_g2m_f5b"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

kafka.metrics.broker

</td><td>

Collects Kafka Broker Metrics from the host.

</td><td>

`commonchecks metric-kafka-broker` \[flags\]Where the flags are:

-   `-J, --javapath` = Java executable path \(default "java"\).
-   `-j, --jmxport` = JMX Port \(default "9999"\)

 Usage example: `commonchecks metric-kafka-broker -J "/usr/bin/java" -j 9999`

</td><td>

hostname.Kafka.Broker.ReplicaManager.IsrExpandsPerSec.OneMinuteRate 0.000

 hostname.Kafka.Broker.DelayedOperationPurgatory.PurgatorySize.Fetch.Value 627.000

 hostname.Kafka.Broker.ControllerStats.UncleanLeaderElectionsPerSec.OneMinuteRate 0.000

 hostname.Kafka.Broker.RequestMetrics.RequestsPerSec.Produce.OneMinuteRate 0.000

</td></tr></tbody>
</table><table id="table_ds2_3fm_f5b"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

kafka.metrics.zookeeper

</td><td>

Collects Zookeeper Metrics from the host.

</td><td>

`commonchecks metric-kafka-zookeeper` \[flags\]Where the flag is: `-p, --adminserverport`= Admin Server Port \(default "8085"\)

 Usage example: `commonchecks metric-kafka-zookeeper -p 8085`

</td><td>

hostname.Kafka.Zookeeper.outstanding\_requests 2.000 1648183249

 hostname.Kafka.Zookeeper.avg\_latency 1.05 1648183249

 hostname.Kafka.Zookeeper.num\_alive\_connections 1.000 1648183249

 hostname.Kafka.Zookeeper.open\_file\_descriptor\_count 124.000 1648183249

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

