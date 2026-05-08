---
title: Sensitive data filters
description: The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Sensitive data filters

The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.

Discovery collects configuration and operational data from servers and applications to populate the CMDB. Some of this data may include sensitive information such as passwords, tokens, or credentials. Storing these values in CMDB can create security and compliance risks. Sensitive data filters enable administrators to define regex filters that identify sensitive information in probe results. When Discovery runs, the probe collects data and processes it on the MID Server. Before the ECC Queue input payload is sent to the instance, the Post Processor script applies transformations and checks for regex filters defined in the Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table. If a match is found, the script redacts the sensitive value in the payload so that only redacted data is transmitted to the instance and stored in CMDB.

For example, if the regex is `(?i)(?:pwd|password|passwd|secret)=(\S+)` and the original content is:

```
user=admin password=MySecret123 host=localhost
```

After redaction, it becomes:

```
user=admin password=REDACTED host=localhost
```

## Requirements

Discovery must be using version XP11, YP10, ZP4 or later.

Visibility Content must be using version 6.29.0.

## Benefits

Benefits of implementing sensitive data filters include:

-   Protect confidential information: Prevent credentials or other sensitive values from appearing in logs or output.
-   Compliance: Support organizational security and privacy standards by meeting requirements.
-   Flexibility: Customize filters to your environment and data sources.

## Examples

Examples of data you can protect with sensitive data filters include:

-   Tracked configuration files: A MySQL configuration file may contain a password. A regex filter can detect the password and redact it.
-   Process parameters: Linux server process arguments may include sensitive tokens. Filters can identify and redact these values.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

