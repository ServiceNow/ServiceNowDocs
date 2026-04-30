---
title: Submit a Health Log Analytics scale request through the Now Support catalog
description: Request Health Log Analytics scaling to support streaming logs at a higher rate. 
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scale HLA to stream logs at a higher rate, Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Submit a Health Log Analytics scale request through the Now Support catalog

Request Health Log Analytics scaling to support streaming logs at a higher rate. 

## Before you begin

Role required: None

## About this task

This procedure explains how to submit a scaling request through the Now Support catalog. You can also contact your ServiceNow account manager to request Health Log Analytics scaling.

## Procedure

1.  On [Now Support](https://support.servicenow.com/), navigate to **All** &gt; **Service Catalog**.

2.  In the Request scale dialog, select the appropriate option:

    -   Install the Health Log Analytics Prime app from the ServiceNow Store.

        When the app is installed, the additional services for supporting your request can use shared resources in other datacenters besides the one hosting your ServiceNow instance. This ability enables better resource allocation for supporting your current and future requests.

        **Note:** To install the Health Log Analytics Prime app, you must accept its terms and conditions.

    -   Request scale without installing the Health Log Analytics Prime app.

        When you select this option, the additional resources for supporting your request reside in the same datacenter as your instance. You may experience some limitations in terms of capacity.

3.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Select instance|The name of your ServiceNow instance.|
    |Number of subscription units|The number of subscription units Health Log Analytics must support.|

4.  Select **Submit**.

    Your scale request is submitted. When it’s approved, ServiceNow notifies you by email.


**Parent Topic:**[Scaling Health Log Analytics to stream logs at a higher rate](../concept/hla-scaling.md)

