---
title: Kafka SSL credentials fields
description: Description of the fields on the Kafka SSL credentials form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Apache Kafka data input configuration fields, Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Kafka SSL credentials fields

Description of the fields on the Kafka SSL credentials form.

|FIeld|Description|
|-----|-----------|
|SSL keystore|The content of an actual server.keystore.jks file, encoded as a Base64 string.|
|SSL keystore type|Format of the SSL keystore file. Default: Java KeyStore \(JKS\).|
|SSL keystore password|Password to the keystore, identical to the value of the ssl.keystore.password property in Apache Kafka.|
|SSL key password|Password, identical to the ssl.key.password property value in Apache Kafka.|
|SSL truststore|The content of an actual client.truststore.jks file, encoded as a Base64 string.|
|SSL truststore type|Format of the truststore file. Default: Java KeyStore \(JKS\).|
|SSL truststore password|Password to the truststore, identical to the value of the ssl.truststore.password property in Apache Kafka.|
|SSL provider|Name of the security provider used for SSL connections.|
|Disable hostname verification|Option to disable verification of the hostname.|
|Additional Kafka consumer properties|Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1|

<table id="table_frn_5tz_htb"><thead><tr><th>

FIeld

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SSL truststore

</td><td>

The content of an actual client.truststore.jks file, encoded as a Base64 string.

</td></tr><tr><td>

SSL truststore type

</td><td>

Format of the SSL truststore file. Default: Java KeyStore \(JKS\).

</td></tr><tr><td>

SSL truststore password

</td><td>

Password to the truststore, identical to the value of the ssl.truststore.password property in Apache Kafka.

</td></tr><tr><td>

SSL provider

</td><td>

Name of the security provider used for SSL connections.

</td></tr><tr><td>

Disable hostname verification

</td><td>

Option to disable verification of the hostname.

</td></tr><tr><td>

User name

</td><td>

The user name, if any, associated with this credential.**Note:** The specified user name is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`

</td></tr><tr><td>

Password

</td><td>

The password associated with this credential.**Note:**

-   The specified password is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`
-   The password you specify is invisible. It is stored in the database in encrypted form.

</td></tr><tr><td>

Additional Kafka consumer properties

</td><td>

Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1

</td></tr></tbody>
</table><table id="table_yjt_wtz_htb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

User name

</td><td>

The user name, if any, associated with this credential.**Note:** The specified user name is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`

</td></tr><tr><td>

Password

</td><td>

The password associated with this credential.**Note:**

-   The specified password is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`
-   The password you specify is invisible. It is stored in the database in encrypted form.

</td></tr><tr><td>

Additional Kafka consumer properties

</td><td>

Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1

</td></tr></tbody>
</table>**Parent Topic:**[Apache Kafka data input configuration fields](hla-data-input-kafka-ref.md)

