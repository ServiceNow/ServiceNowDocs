---
title: Create troubleshooting agent system property
description: Create a system property to enable access to the Flow Troubleshooting Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-troubleshooting-agent-system-property.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create troubleshooting agent system property

Create a system property to enable access to the Flow Troubleshooting Agent.

## Before you begin

Role required: admin

## About this task

Adding or changing a system property can affect your system performance. For more information about system properties, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select **New**.

3.  Complete the System Property form using these values.

    |Field|Value|
    |-----|-----|
    |Name|com.glide.hub.flow.launch\_troubleshooting\_agent|
    |Application|Global|
    |Type|true \| false|
    |Value|true|
    |Ignore cache|true|

4.  Select **Submit**.


## Result

The system displays the **Troubleshoot** button in flow execution details and ServiceNow Otto conversations can launch the Flow Troubleshooting Agent.

