---
title: Active Directory metrics
description: The following table lists the metrics that are gathered as output from Active Directory checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Active Directory metrics

The following table lists the metrics that are gathered as output from Active Directory checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|active\_dir.DRA\_Inbound\_Bytes\_after\_compressed/sec| | |Shows the compressed size of inbound compressed replication data \(size after compression, from DSAs in other sites\).|
|active\_dir.DRA\_Inbound\_Bytes\_before\_compressed/sec| | |Shows the original size of inbound compressed replication data \(size before compression, from DSAs in other sites\).|
|active\_dir.DRA\_Inbound\_Bytes\_not\_compressed/sec| | |Shows the number of incoming bytes replicated that were not compressed at the source \(that is, from DSAs in the same site\).|
|active\_dir.DRA\_Inbound\_Bytes\_Total/sec \(featured metric\)| | |Shows the total number of bytes replicated in. This counter is the sum of the number of uncompressed bytes \(never compressed\) and the number of compressed bytes \(after compression\).|
|active\_dir.DRA\_Inbound\_Full\_Sync\_Objects\_Remaining \(featured metric\)| | |Shows the number of objects remaining until the full synchronization is completed \(when set\).|
|active\_dir.DRA\_Inbound\_Object\_Updates\_Remaining\_in\_Packet| | |Shows the number of object updates received in the current directory replication update packet that have not yet been applied to the local server.|
|active\_dir.DRA\_Inbound\_Objects/sec| | |Shows the rate at which replication updates received from replication partners are applied by the local directory service. This counter excludes changes that are received but not applied \(because, for example, the change has already been made\). This indicates how much replication update activity is occurring on the server as a result of changes generated on other servers.|
|active\_dir.DRA\_Inbound\_Objects\_Applied/sec| | |Shows the number of objects received from inbound replication partners that contained no updates that needed to be applied.|
|active\_dir.DRA\_Inbound\_Objects\_Filtered/sec| | |Shows the number of objects received from neighbors through inbound replication. A neighbor is a domain controller from which the local domain controller replicates locally.|
|active\_dir.DRA\_Inbound\_Properties\_Applied/sec| | |Shows the number of properties that are updated due to the incoming property's winning the reconciliation logic that determines the final value to be replicated.|
|active\_dir.DRA\_Inbound\_Properties\_Filtered/sec| | |Shows the number of property changes that are received during the replication that we have already seen.|
|active\_dir.DRA\_Inbound\_Properties\_Total/sec| | |Shows the total number of object properties received from inbound replication partners.|
|active\_dir.DRA\_Inbound\_Values\_DNs/sec| | |Shows the number of object property values received from inbound replication partners that are distinguished names \(DNs\) that reference other objects. DN values, such as group or distribution list memberships, are generally more expensive to apply than other kinds of values.|
|active\_dir.DRA\_Inbound\_Values\_Total/sec| | |Shows the total number of object property values received from inbound replication partners. Each inbound object has one or more properties, and each property has zero or more values. Zero values indicate property removal.|
|active\_dir.DRA\_Outbound\_Bytes\_after\_compressed/sec| | |Shows the compressed size of outbound compressed replication data \(size after compression, from DSAs in other sites\).|
|active\_dir.DRA\_Outbound\_Bytes\_before\_compressed/sec| | |Shows the original size of outbound compressed replication data \(size before compression, from DSAs in other sites\).|
|active\_dir.DRA\_Outbound\_Bytes\_not\_compressed/sec| | |Shows the number of bytes replicated out that were not compressed \(that is, from DSAs in the same site\).|
|active\_dir.DRA\_Outbound\_Bytes\_Total/sec \(featured metric\)| | |Shows the total number of bytes replicated out. This counter is the sum of the number of uncompressed bytes \(never compressed\) and the number of compressed bytes \(after compression\).|
|active\_dir.DRA\_Outbound\_Objects/sec| | |Shows the number of objects that were determined by outbound replication to have no updates that the outbound partner did not already have.|
|active\_dir.DRA\_Outbound\_Objects\_Filtered/sec| | |Shows the number of objects replicated out.|
|active\_dir.DRA\_Outbound\_Properties/sec| | |Shows the number of properties replicated out.|
|active\_dir.DRA\_Outbound\_Values\_DNs/sec| | |Shows the number of object property values containing DNs sent to outbound replication partners. DN values, such as group or distribution list memberships, are generally more expensive to read than other kinds of values.|
|active\_dir.DRA\_Outbound\_Values\_Total/sec| | |Shows the number of object property values sent to outbound replication partners.|
|active\_dir.DRA\_Pending\_Replication\_Synchronizations| | |Shows the number of directory synchronizations that are queued for this server but not yet processed.|
|active\_dir.DRA\_Sync\_Requests\_Made| | |Shows the number of synchronization requests made to neighbors.|
|active\_dir.DS\_Threads\_in\_Use \(featured metric\)| | |Shows the current number of threads in use by the directory service \(which is different from the number of threads in the directory service process\). This is the number of threads currently servicing client API calls; it can be used to indicate whether additional processors should be used.|
|active\_dir.LDAP\_Bind\_Time \(featured metric\)| | |Shows the time, in milliseconds, taken for the last successful LDAP bind.|
|active\_dir.LDAP\_Client\_Sessions \(featured metric\)| | |Shows the number of currently connected LDAP client sessions.|
|active\_dir.LDAP\_Searches/sec \(featured metric\)| | |Shows the rate at which LDAP clients perform search operations.|
|active\_dir.LDAP\_Successful\_Binds/sec \(featured metric\)| | |Shows the number of LDAP binds per second.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

