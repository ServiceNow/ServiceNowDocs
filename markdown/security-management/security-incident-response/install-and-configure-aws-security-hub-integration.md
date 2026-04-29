---
title: Install and configure the AWS Security Hub integration
description: Install and configure the AWS Security Hub integration from the ServiceNow Store on your ServiceNow AI Platform instance to start ingesting AWS Security Hub findings.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the AWS Security Hub integration

Install and configure the AWS Security Hub integration from the ServiceNow Store on your ServiceNow AI Platform instance to start ingesting AWS Security Hub findings.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Download the AWS Security Hub integration from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the AWS Security Hub tile and click **Configure**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the AWS Security Hub instance configuration.|
    |Region name|Region you assigned in the ServiceNow® user profile on AWS Security Hub portal.|
    |Secret Key|Secret key you created for the ServiceNow® user profile on AWS Security Hub portal.|
    |Access Key|Access key you created for the ServiceNow® user profile on AWS Security Hub portal.|

5.  Click **Submit**.


## Result

After you successfully validate and submit the configuration, each Security Hub findings ingestion server configuration is saved on the Security Integrations page as a tile.

