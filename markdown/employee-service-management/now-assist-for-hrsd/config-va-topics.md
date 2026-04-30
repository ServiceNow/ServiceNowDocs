---
title: Configure the Now Assist for HRSD Virtual Agent topics
description: Complete the configuration steps to enable your employees place requests to the Human Capital Management \(HCM\) system using the Now Assist for HRSD Virtual Agent topics in Employee Center.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure the Now Assist for HRSD Virtual Agent topics

Complete the configuration steps to enable your employees place requests to the Human Capital Management \(HCM\) system using the Now Assist for HRSD Virtual Agent topics in Employee Center.

## Before you begin

Role required: flow\_designer, decision\_table\_admin, sn\_hr\_integr\_fw.admin, and sn\_hr\_core.admin

## Procedure

1.  Install the Now Assist for HRSD and Enterprise Service Management Integrations Framework \(v3.6\) applications from ServiceNow Store.

2.  Configure the required ServiceNow spokes or customize spokes to pull data from HCM systems.

3.  Create subflows for provider aligning with Template Integration Gateway.

    See [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:**

    -   Subflows have been created for Oracle HCM, except for the Request Time off and Add Expense Virtual Agent topics. The Virtual Agent experience has been provided for the Request Time off and Add Expense topics, but without the back-end support through subflows. For more information on the default Virtual Agent topics, see [Now Assist for HRSD Virtual Agent topics](../concept/now-assist-ohcm.md).
    -   The subflows for Oracle HCM can be used as a reference to build subflows for any other HCM systems.
4.  [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md) by adding input choices, configuring conditions on input choices and results.

5.  Create a Virtual Agent topic block:

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
    2.  From the **LLM Assistant** list, select **Now Assist in Virtual Agent**.
    3.  Filter the topics by setting the category to **Now assist for HR service Delivery**.
    4.  Select a Virtual Agent topic.
        1.  Edit topic properties and make the necessary edits in the topic, such as update the node name, and response message.
        2.  In Integration Gateway, specify the appropriate feature, service name, user, and make the necessary edits.

            **Note:** To publish the Virtual Agent topics in Now Assist for HRSD, publish these topic blocks: **Get Authentication** and **Process Integration Errors**.


## What to do next

When an Virtual Agent topic invokes the Integration Gateway subflow, the subflow reviews input values in Integration Provider Mapping \(Decision table\) to execute results.

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

