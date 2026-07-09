---
title: Configure triggers in ServiceNow instance
description: Configure endpoint for webhooks in the Jenkins that support the token authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/jenkinsv2-conf-triggers-s.html
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

    \[Omitted image "image.jenkinsv2-ext-triggers1"\] Alt text:

5.  For the **JenkinsV2 External Trigger** end point, click **Configure**.

    \[Omitted image "image.jenkinsv2-ext-triggers2"\] Alt text:

6.  Select the user who can trigger the endpoint and click **Activate**.

    \[Omitted image "image.jenkinsv2-ext-trig3"\] Alt text:

7.  Copy the generated endpoint URL.

    \[Omitted image "image.jenkinsv2-ext-trig4"\] Alt text:


