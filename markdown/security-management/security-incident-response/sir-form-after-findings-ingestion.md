---
title: SIR form after an AWS Security Hub finding ingestion
description: After the ServiceNow AI Platform ingests the AWS Security Hub finding, a security incident is created and the updates are made to that security incident record.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# SIR form after an AWS Security Hub finding ingestion

After the ServiceNow AI Platform ingests the AWS Security Hub finding, a security incident is created and the updates are made to that security incident record.

## Work notes

A work note is posted when an incident is aggregated and if you have configured the **Log work note for new finding** option in the [Define filter and aggregation criteria for AWS Security Hub findings ingestion](aws-security-hub-profile-filter-and-aggregation-criteria.md#).

You can also view the internal finding import record that contains the raw incident data.

When you click the **Click here** link, you can view the record in the AWS Security Hub environment. The following example shows the record in the AWS Security Hub environment.

## Aggregated AWS Security Hub findings

View Aggregated AWS Security Hub findings: View the incidents that are aggregated to the security incident. Navigate to **Show All Related Lists** &gt; **Aggregated AWS Security Hub findings**.

Create security incident: Select an incident from the list, click the **Actions** menu, and then click **Create security incident**. This option creates a new security incident for the incident and this incident is de-aggregated from the parent security incident.

