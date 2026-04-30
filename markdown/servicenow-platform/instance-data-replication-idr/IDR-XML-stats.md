---
title: Instance Data Replication XML stats
description: Extract Instance Data Replication \(IDR\)-related data from your instance to monitor replication status.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Instance Data Replication XML stats

Extract Instance Data Replication \(IDR\)-related data from your instance to monitor replication status.

## IDR XML Stats

You can view key metrics from your IDR producer and consumer instances to monitor performance and the status of IDR processing.

In a browser where the instance is running, append the following text to the instance URL: `xmlstats.do?include=idr`. The following output is an example of the IDR XML stats.

```
<idr status="enabled">
<producer producer_last_run="2020-11-06 13:45:30" 
replication_queue_position="data_replication_queue0001@2020-11-05T22:58:32Z,2732,0,1" 
replication_queue_reading_lag="00:01:00">
<replset last_message_sent_on="2020-11-06 13:44:31" 
last_position="data_replication_queue0001@2020-11-05T22:58:32Z 2731,0,1" 
last_sent_message_id="f339a84ac818201050bec7cf110d4135" name="N-2NormalStickyReplicaiton" 
status="active" topic_name="d59f4226db6680504d2bac44d49619a0.570532d91b582010ef39fcc4cc4bcba1">
<subscriber name="persistencetestingora9" remote="false"/>
</replset>
<replset last_message_sent_on="2020-11-06 13:44:31" 
last_position="data_replication_queue0001@2020-11-05T22:58:32Z,2732,0,1" 
last_sent_message_id="7f39a84ae5182010fad1a90f50fcd335" 
name="N-1NormalTransformerReplication" 
status="active" 
topic_name="d59f4226db6680504d2bac44d49619a0.6f0572d91b582010ef39fcc4cc4bcb01"/>
</producer>
<consumer consumer_last_run="2020-11-11 14:22:36">
<replset data_lag="00:00:22" last_heartbeat_received_on="2020-11-11 14:22:36" last_message_received_network_time="00:00:05" 
last_position="data_replication_queue0002@2020-11-11T18:50:47Z,212,0,1" name="N-2NormalTransformerReplication" 
producer_name="byungidrorlandonightlyconsumer6" remote="false" status="active" topic_name="07f85510db93005407072f17d496196a.21247ddddb182010ed02e3e2ca9619c9"/>
<replset data_lag="00:00:22" last_heartbeat_received_on="2020-11-11 14:22:36" last_message_received_network_time="00:00:06" 
last_position="data_replication_queue0000@2020-11-10T23:28:58Z,1374,0,1" name="N-1NormalStickyReplication" 
producer_name="byungidrparis1" remote="false" status="active" topic_name="559cd6d2db6ad458a667cac505961973.bdc33951db9020107cfe200c0b9619ea"/>
</consumer>
</idr>
```

|Metric|Description|
|------|-----------|
|**idr status**|Shows whether IDR is enabled for your instance.|
|Producer instance| |
|**producer producer\_last\_run**|The last time that the **IDRProducerJob** scheduled job ran \(GMT\).|
|**producer replication\_queue\_position**|Position of the cursor in the replication queue.|
|replication\_queue\_reading\_lag|The time between when a change is made, and when the **IDRProducerJob** scheduled job sends that change to the network.|
|replset last\_message\_sent\_on|The last time data was sent to the network from this replication set.|
|replset last\_position|The cursor position in the data\_replication\_queue when the last message was sent for this replication set.|
|last\_sent\_message\_id|The message ID of the last sent message from the data\_replication\_queue.|
|name|The name of the replication set.|
|status|The replication set status.|
|topic\_name|The topic name in the message queue for this replication set.|
|Consumer instance| |
|consumer\_last\_run|The last time the **IDRConsumerJob** scheduled job \(local\) or **IDRDeltaConsumerJob-&lt;instanceid&gt;** scheduled job \(remote\) ran \(GMT\).|
|replset data\_lag|Time since the last heartbeat was received. Heartbeats should occur every minute for a replication set.|
|last\_heartbeat\_received\_on|Time of the last heartbeat for this replication set.|
|last\_message\_received\_network\_time|For the last received message, the time difference between when it was sent to the message queue and when it was picked up by the consumer instance.|
|replset last\_position|The cursor position in the data\_replication\_queue, at which the last message was sent for this replication set.|
|name|The name of the replication set.|
|status|The replication set status.|
|topic\_name|The topic name in the message queue for this replication set.|

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](common-issues-idr.md)

