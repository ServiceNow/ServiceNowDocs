---
title: Email performance metrics
description: The metrics provide the Email performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-emails-performance-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 3
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Email performance metrics

The metrics provide the Email performance snapshot within the ServiceNow AI Platform®.

## Inbound Emails

This represents the total number of emails received. These emails are either in processed, ignored or failed states. Processed means the emails were successfully processed by email reader, Ignored means the emails were successfully ignored by email reader and failed means the email reader was failed to process the inbound email.

The processed inbound email metric values may reach in 1000s if the instance has implementation of applications that process emails as part of the workflow. If the value gets too low, when otherwise it is high, it is likely to indicate an issue with inbound email reader and should be further investigated to remediate.

## Outbound Emails

his represents the total number of emails processed by the SMTP server. This includes emails sent, emails ignored while sending, emails ignored, and emails failed to send by SMTP server. This also includes number of emails that are in a Ready state since the previous data collection point \(that is, in the previous 2 seconds\) but not processed by SMTP server yet.

If the emails sent is zero, then it means that the SMTP server has nothing further to process or there has been a failure in the SMTP server.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

[Database performance metrics]()

[Semaphores performance metrics]()

[Event queues performance metrics]()

[ECC Queue performance metrics]()

[Scheduler performance metrics]()

[Job details performance metrics]()

[Node health performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

