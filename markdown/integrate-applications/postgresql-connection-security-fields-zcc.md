---
title: PostgreSQL connection security configuration fields
description: Fields that appear under Connection security configurations on the New PostgreSQL Connection form when SSL is set to Enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/postgresql-connection-security-fields-zcc.html
release: australia
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [PostgreSQL, SSL, connection security configurations, zero copy connector]
breadcrumb: [Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# PostgreSQL connection security configuration fields

Fields that appear under Connection security configurations on the New PostgreSQL Connection form when SSL is set to Enabled.

## SSL mode: TLS \(verify-ca\)

|Condition|Field|Description|
|---------|-----|-----------|
|Server Certificate Source: Default \(JVM CA\)|—|No additional fields.|
|Server Certificate Source: Custom CA|Store type|Format of the truststore. Confirmed values: PEM, JKS, PKCS12.|
|Server Certificate Source: Custom CA|Truststore|File containing the certificate\(s\) used to verify the PostgreSQL server's identity. Required for all Store type values.|
|Server Certificate Source: Custom CA|Truststore password|Password for the truststore file. Required when Store type is JKS or PKCS12; not required when Store type is PEM.|

## SSL mode: mTLS

|Condition|Field|Description|
|---------|-----|-----------|
|Store type: PEM|Keystore password|Password for the client certificate/private key. Not required when Store type is PEM.|
|Store type: PEM|Client Certificate|File containing the client certificate presented to the PostgreSQL server. Required.|
|Store type: PEM|Client private key|File containing the client private key paired with the Client Certificate. Not required.|
|Store type: JKS or PKCS12|Keystore password|Password for the keystore file. Required.|
|Store type: JKS or PKCS12|Keystore|File containing the client certificate and private key in a single keystore container. Required.|
|\(any Store type\)|Server Certificate Source|Confirmed values: Default \(JVM CA\), Custom CA.|
|Server Certificate Source: Custom CA|Truststore|File containing the certificate\(s\) used to verify the PostgreSQL server's identity. Required.|
|Server Certificate Source: Custom CA|Truststore password|Password for the truststore file. Required when Store type is JKS or PKCS12; not required when Store type is PEM.|

**Parent Topic:**[Zero Copy Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/reference-zcc.md)

**Related topics**  


[Create a PostgreSQL connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-postgresql-connection-zcc.md)

