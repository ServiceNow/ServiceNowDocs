---
title: Configure the chunk size of Microsoft Azure billing blob
description: Reduce the time required to download Azure billing files by defining the chunk size of a blob.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configure the chunk size of Microsoft Azure billing blob

Reduce the time required to download Azure billing files by defining the chunk size of a blob.

## Before you begin

Role required: admin

## About this task

**Important:** This task is applicable only if you have installed the Cloud Cost Management Infra Stack application along with Cloud Cost Management version 8.1.

A single Azure billing blob can be large, resulting in performance issues during the download. If you have installed the Cloud Cost Management Infra Stack application, bill processing only happens on the Kubernetes cluster that's outside Glide but within ServiceNow datacenters. This new framework with Kubernetes cluster supports parallel processing of multiple chunks of blobs, making the billing file download faster. You can also set the system property **sn\_cld\_intg\_azure.billing\_chunk\_duration** to specify the duration in number of days for which the billing data will be included in each chunk.

## Procedure

1.  Open the System properties table by entering `sys_properties.list` in the application filter.

2.  Filter the list to open the **sn\_cld\_intg\_azure.billing\_chunk\_duration** property.

    The default value is 3, which means that each blob contains three days billing data.

3.  Modify the value as needed.

    **Note:** Performance improves by setting the property to a value below 3.

4.  Save the property.


