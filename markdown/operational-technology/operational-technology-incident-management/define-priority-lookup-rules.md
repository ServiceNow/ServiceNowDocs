---
title: Define a priority lookup rule for incidents
description: Define the impact and urgency of an Operational Technology incident to calculate its priority. You can then use the priority calculation to prioritize your work and to drive service level agreements \(SLAs\) in your organization.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Define a priority lookup rule for incidents

Define the impact and urgency of an Operational Technology incident to calculate its priority. You can then use the priority calculation to prioritize your work and to drive service level agreements \(SLAs\) in your organization.

## Before you begin

Role required: ot\_incident\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Operational Technology Incident Management** &gt; **Priority Lookup Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Impact|Measure of the effect of an incident on business processes.|
    |Urgency|Measure how long the resolution can be delayed until an incident has a significant business impact.|
    |Priority|Option that is based on the impact and urgency. The priority identifies how quickly the OT engineer should address the task.|
    |Application|Scope of the rules. The scope defines whether the rules are available for all applications or for scoped applications.|
    |Active|Option to define whether the rule is active or not.|
    |Order|Order in which the rules appear in the priority lookup list. This field indicates which rule to execute first.|

    **Note:**

    The priority is calculated according to the sample data lookup rules in the following table.

    |Impact|Urgency|Priority|
    |------|-------|--------|
    |1 - High|1 - High|1 - Critical|
    |1 - High|2 - Medium|2 - High|
    |1 - High|3 - Low|3 - Moderate|
    |2 - Medium|1 - High|2 - High|
    |2 - Medium|2 - Medium|3 - Moderate|
    |2 - Medium|3 - Low|4 - Low|
    |3 - Low|1 - High|3 - Moderate|
    |3 - Low|2 - Medium|4 - Low|
    |3 - Low|3 - Low|5 - Planning|

    By default, the **Priority** field is read-only and must be set by selecting the **Impact** and **Urgency** values. To change how the priority is calculated, you can either alter the priority lookup rules or disable the **Priority is managed by Data Lookup - set as read-only** UI policy and create their own business logic.

4.  Select **Submit**.


**Parent Topic:**[Configuring Operational Technology Incident Management](../concept/configuring-operational-technology-incident-mgt.md)

