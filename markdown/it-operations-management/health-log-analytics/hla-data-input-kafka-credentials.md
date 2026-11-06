---
title: Kafka SSL credentials fields
description: Description of the fields on the Kafka SSL credentials form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/health-log-analytics/hla-data-input-kafka-credentials.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Apache Kafka data input configuration fields, Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Kafka SSL credentials fields

Description of the fields on the Kafka SSL credentials form.

|Field|Description|
|-----|-----------|
|SSL keystore|The content of an actual server.keystore.jks file, encoded as a Base64 string. This field is mandatory.|
|SSL keystore type|Format of the SSL keystore file. Default: Java KeyStore \(JKS\).|
|SSL keystore password|Password to the keystore, identical to the value of the ssl.keystore.password property in Apache Kafka. This field is mandatory.|
|SSL key password|Password, identical to the ssl.key.password property value in Apache Kafka. This field is mandatory.|
|||
|SSL truststore|The content of an actual client.truststore.jks file, encoded as a Base64 string. This field is mandatory.|
|SSL truststore type|Format of the truststore file. Default: Java KeyStore \(JKS\).|
|SSL truststore password|Password to the truststore, identical to the value of the ssl.truststore.password property in Apache Kafka. This field is mandatory.|
|SSL provider|Name of the security provider used for SSL connections.|
|Disable hostname verification|Option to disable verification of the hostname.|
|Additional Kafka consumer properties|Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1|

<table id="table_frn_5tz_htb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SSL truststore

</td><td>

The content of an actual client.truststore.jks file, encoded as a Base64 string. This field is mandatory.

</td></tr><tr><td>

SSL truststore type

</td><td>

Format of the SSL truststore file. Default: Java KeyStore \(JKS\).

</td></tr><tr><td>

SSL truststore password

</td><td>

Password to the truststore, identical to the value of the ssl.truststore.password property in Apache Kafka. This field is mandatory.

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

The user name, if any, associated with this credential. This field is mandatory.**Note:** The specified user name is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`

</td></tr><tr><td>

Password

</td><td>

The password associated with this credential. This field is mandatory.**Note:**

-   The specified password is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`
-   The password you specify is invisible. It is stored in the database in encrypted form.

</td></tr><tr><td>

SASL Mechanism

</td><td>

The SASL authentication mechanism to be used by the Kafka client. The options are:-   PLAIN \(default\)
-   SCRAM-SHA-256
-   SCRAM-SHA-512
-   OAUTHBEARER

This field is mandatory.

</td></tr><tr><td>

SASL JAAS config template

</td><td>

The JAAS configuration to be used by the Kafka client, with the placeholders $\[username\] for the username, and $\[password\] for the password. This field is mandatory.

</td></tr><tr><td>

Additional Kafka consumer properties

</td><td>

Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1

</td></tr></tbody>
</table><table id="table_yjt_wtz_htb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User name

</td><td>

The user name, if any, associated with this credential. This field is mandatory.**Note:** The specified user name is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`

</td></tr><tr><td>

Password

</td><td>

The password associated with this credential. This field is mandatory.**Note:**

-   The specified password is used for SASL authentication using JAAS. The following JAAS configuration is passed to the Kafka Server: `org.apache.kafka.common.security.plain.PlainLoginModule required username=<user_name> password=<password>`
-   The password you specify is invisible. It is stored in the database in encrypted form.

</td></tr><tr><td>

Additional Kafka consumer properties

</td><td>

Semicolon-separated string of additional Kafka consumer properties. For example: ssl.protocol=TLSv1.2;ssl.enabled.protocols=TLSv1.2,TLSv1.1

</td></tr></tbody>
</table>**Parent Topic:**[Apache Kafka data input configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/health-log-analytics/hla-data-input-kafka-ref.md)

