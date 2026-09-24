---
title: Properties installed with Log Export Service
description: Log Export Service \(LES\) adds the following instance system properties and MID Server properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/properties-installed-with-les.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Reference, Log Export Service \(LES\), Platform Security]
---

# Properties installed with Log Export Service

Log Export Service \(LES\) adds the following instance system properties and MID Server properties.

## System properties

Log Export Service adds the following instance system properties.

<table id="table-les-instance-props"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.script.glide\_record\_logger.forward\_tables

</td><td>

String

</td><td>

Comma-separated list of tables that Log Export Service is allowed to forward. Only tables in this list are available as a source type Table on the Log Export Service Source form.

 Default value: `syslog,sys_outbound_http_log,syslog_transaction,sys_audit`

</td></tr><tr><td>

glide.les.disable\_logs\_forwarding

</td><td>

true \| false

</td><td>

Kill switch that turns off Log Export Service auto-configuration and log forwarding globally. When set to `true`, Log Export Service stops forwarding logs to the Hermes Messaging Service.

**Important:** If this property does not exist in the sys\_properties list, create a new property with the same name.

For more information, see [Update system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/update-system-property.md)

 Default value: false

</td></tr><tr><td>

glide.les.max\_queue\_size

</td><td>

Integer

</td><td>

Maximum number of log entries that can wait in the asynchronous forwarding queue. Increase this value if log entries are being dropped under sustained high volume.

 Default value: 4096

</td></tr><tr><td>

glide.les.queue\_slot\_wait\_time

</td><td>

Integer

</td><td>

Time in milliseconds that the Log Export Service appender waits for a free slot in the asynchronous forwarding queue before dropping a log entry. A value of `0` means the appender doesn't wait and drops the entry immediately when the queue is full.

 Default value: 0

</td></tr><tr><td>

glide.log.forwarding.num\_topic\_partitions

</td><td>

Integer

</td><td>

Number of partitions created for each Hermes topic that Log Export Service produces to. Partitions affect scalability and parallelism of downstream consumers.

 Default value: 4

</td></tr><tr><td>

glide.log.forwarding.syslog.topics.limit

</td><td>

Integer

</td><td>

Maximum number of unique Hermes topics that can be created for the syslog source.

 Default value: 10

</td></tr><tr><td>

glide.log.les.async\_enabled

</td><td>

true \| false

</td><td>

Enables asynchronous log forwarding from the instance to the Hermes Messaging Service. Asynchronous forwarding reduces the performance impact on the instance under high log volume.

 Default value: true

</td></tr><tr><td>

sn\_logstoanalytics.debug

</td><td>

true \| false

</td><td>

Enables verbose debug logging for the Log Export Service application.

 Default value: false

 **Important:** This property is disabled by default to prevent unnecessary debug logs in node logs.

</td></tr><tr><td>

sn\_logstoanalytics.kafka.multi\_topics

</td><td>

true \| false

</td><td>

When set to `true`, Log Export Service uses a separate Kafka topic for each source type instead of a shared topic, so that downstream consumers can subscribe to specific log sources independently.

**Important:** When set to `false`, the ability to create multi topics in the source table is disabled.

 Default value: false

</td></tr></tbody>
</table>## MID Server properties

For deployments that use a dedicated MID Server to consume logs from the Hermes Messaging Service, Log Export Service uses the following MID Server properties.

<table id="table-les-mid-props"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.les.consumer.threads.count

</td><td>

Integer

</td><td>

Number of Kafka consumer threads that read from Hermes topics on the MID Server. Controls the number of parallel consumers.

 Default value: 4

</td></tr><tr><td>

mid.les.kafka.bootstrap.servers

</td><td>

String

</td><td>

Comma-separated list of `host:port` pairs for the primary Hermes Kafka cluster. The default port range is 4100-4150; ensure this range is open between the MID Server and Hermes.

</td></tr><tr><td>

mid.les.kafka.client.id

</td><td>

String

</td><td>

Kafka client identifier the MID Server sends when opening a connection to Hermes. This value appears in Kafka client logs. Set the value to the ServiceNow AI Platform instance name.

</td></tr><tr><td>

mid.les.kafka.enable.auto.commit

</td><td>

true \| false

</td><td>

Enables Kafka automatic offset commits. Keep this property set to `false` so that offsets are committed only after successful message processing, which helps prevent data loss if the consumer restarts mid-batch.

 Default value: false

</td></tr><tr><td>

mid.les.kafka.group.id

</td><td>

String

</td><td>

Kafka consumer group identifier that the MID Server joins when consuming from Hermes. This value must be unique per consumer group. Set the value to `snc.<instance_name>.group1`.

</td></tr><tr><td>

mid.les.kafka.poll.duration.millis

</td><td>

Integer

</td><td>

Time in milliseconds that the consumer waits while polling Kafka for new records. Higher values reduce polling overhead but slightly increase latency.

 Default value: 1000

</td></tr><tr><td>

mid.les.kafka.security.protocol

</td><td>

String

</td><td>

Security protocol used for the Kafka connection to Hermes. Log Export Service supports SSL. Set the value to `SSL`.

</td></tr><tr><td>

mid.les.kafka.set2.bootstrap.servers

</td><td>

String

</td><td>

Comma-separated list of `host:port` pairs for the secondary Hermes Kafka cluster, used for high availability and failover. The default port range is 4200-4250.

</td></tr><tr><td>

mid.les.kafka.ssl.key.password

</td><td>

String

</td><td>

Password for the private key stored inside the keystore file.

</td></tr><tr><td>

mid.les.kafka.ssl.keystore.location

</td><td>

String

</td><td>

Absolute file path on the MID Server host to the PKCS12 keystore that contains the MID Server client certificate presented to Hermes. For example, `/opt/mid/certs/mid_keystore.p12`.

</td></tr><tr><td>

mid.les.kafka.ssl.keystore.password

</td><td>

String

</td><td>

Password that unlocks the keystore file specified in **mid.les.kafka.ssl.keystore.location**.

</td></tr><tr><td>

mid.les.kafka.ssl.keystore.type

</td><td>

String

</td><td>

Format of the keystore file. Typically `PKCS12`.

 Default value: PKCS12

</td></tr><tr><td>

mid.les.kafka.ssl.truststore.location

</td><td>

String

</td><td>

Absolute file path on the MID Server host to the PKCS12 truststore that contains the Hermes CA certificates. For example, `/opt/mid/certs/mid_truststore.p12`.

</td></tr><tr><td>

mid.les.kafka.ssl.truststore.password

</td><td>

String

</td><td>

Password that unlocks the truststore file specified in **mid.les.kafka.ssl.truststore.location**.

</td></tr><tr><td>

mid.les.kafka.ssl.truststore.type

</td><td>

String

</td><td>

Format of the truststore file. Typically `PKCS12`.

 Default value: PKCS12

</td></tr><tr><td>

mid.les.metrics.frequency.millis

</td><td>

Integer

</td><td>

Frequency in milliseconds at which the MID Server reports Log Export Service consumer metrics back to the instance.

 Default value: 60000 \(60 seconds\)

</td></tr><tr><td>

mid.les.processor.threads.count

</td><td>

Integer

</td><td>

Number of worker threads used to process consumed messages. Can be tuned independently from **mid.les.consumer.threads.count** to increase throughput without changing the number of Kafka pollers.

 Default value: 4

</td></tr></tbody>
</table>**Parent Topic:**[Log Export Service \(LES\) references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-references.md)

**Related topics**  


[Log Export Service roles]()

[Log Export Service actions and required roles]()

