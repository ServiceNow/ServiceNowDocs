---
title: Disable deprecated TLS versions
description: Avoid loss or leakage of sensitive data by disabling deprecated TLS versions.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-18"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Disable deprecated TLS versions

Avoid loss or leakage of sensitive data by disabling deprecated TLS versions.

Confirm that your instance only negotiates for communication via Transport Layer Security \(TLS\) versions 1.2 when communicating with other servers to help prevent data transfer over weaker TLS 1 and TLS 1.1 protocol versions.

Set the **com.glide.communications.disable.deprecated.tls** to **true** to use only TLS versions 1.2 and up.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|com.glide.communications.disable.deprecated.tls|
|Plugin applicability|None|
|Security risk|Using outdated and unsupported TLS versions could result in loss and leakage of sensitive data.|
|Common Vulnerability Scoring System \(CVSS\) score|4.4|
|Common Vulnerability Scoring System \(CVSS\) rating|Medium|
|Functional impact|When this property is set to **true**, older insecure servers that require a weaker TLS 1 or 1.1 protocol aren’t able to communicate with your instance.|
|Dependencies and prerequisites|None|
|Data type|Boolean|
|Base system value|true|
|Fallback value|true|
|Recommended value|true|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Communications](sc-communications.md)

