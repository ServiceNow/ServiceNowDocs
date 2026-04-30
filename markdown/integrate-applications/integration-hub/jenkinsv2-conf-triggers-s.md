---
title: Configure triggers in ServiceNow instance
description: Configure endpoint for webhooks in the Jenkins that support the token authentication.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-28"
reading_time_minutes: 1
breadcrumb: [Set up triggers for the Jenkins spoke, Jenkins v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure triggers in ServiceNow instance

Configure endpoint for webhooks in the Jenkins that support the token authentication.

## Before you begin

Role required: flow\_designer and connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **JenkinsV2 Spoke** endpoint and click **View Details**.

    ![image.jenkinsv2-ext-triggers1]

5.  For the **JenkinsV2 External Trigger** end point, click **Configure**.

    ![image.jenkinsv2-ext-triggers2]

6.  Select the user who can trigger the endpoint and click **Activate**.

    ![image.jenkinsv2-ext-trig3]

7.  Copy the generated endpoint URL.

    ![image.jenkinsv2-ext-trig4]


