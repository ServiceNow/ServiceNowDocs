---
title: Components installed with the GRC: Metrics application
description: The GRC: Metrics application adds roles that are listed here.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Components installed with the GRC: Metrics application

The GRC: Metrics application adds roles that are listed here.

## Roles installed

The following roles are installed with the GRC: Metrics application.

|Role|Description|Contains|
|----|-----------|--------|
|sn\_grc\_metric.admin|This role serves as the Administrator within the application, and contains the responsibilities of the Metric Manager role. The role possesses the ability to override metric data results in metric data tasks and has the authority to delete metric definitions and metrics. Typically, this role is assigned to individuals holding positions as product owners or application administrators.|sn\_grc\_metric.manager, schedule\_admin|
|sn\_grc\_metric.manager|This role possesses the ability read, create, and update metric definitions and metrics. It is primarily assigned to risk managers, compliance managers, or business managers, who require the authority to define metrics within their respective areas of responsibility.|sn\_grc\_metric.user|
|sn\_grc\_metric.reader|This role is restricted to read-only access. It does not possess the privileges to create, edit, or update any metric definitions or metrics. However, as a metric reader, this role is authorized to review and approve metric data tasks where they have been designated as an approver. This role can be assigned to managers and executives if they want to access dashboards with metrics data to monitor the performance of the metrics.|None|
|sn\_grc\_metric.user|This role is primarily assigned to data owners, enabling them to respond to manual metric data entry tasks. Typically, these users are from the business and hold ownership responsibilities within the organization.|sn\_grc.reader, sn\_grc\_metric.reader|
|sn\_grc\_metric.developer|Users with this role possess the privilege to write and edit the script for data collection automated metric definition.|None|

**Parent Topic:**[GRC: Metrics reference](../concept/grc-metrics-reference-irm.md)

