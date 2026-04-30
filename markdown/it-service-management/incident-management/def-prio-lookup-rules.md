---
title: Define priority lookup rules
description: Define impact and urgency of an incident to calculate the priority. The priority calculation can then be used to prioritize work and drive service level agreements.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Incident Management, IT Service Management]
---

# Define priority lookup rules

Define impact and urgency of an incident to calculate the priority. The priority calculation can then be used to prioritize work and drive service level agreements.

## Before you begin

Role required: data\_lookup\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Priority Lookup Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Impact|Impact is a measure of the effect of an incident, problem, or change on business processes.|
    |Urgency|Urgency is a measure of how long the resolution can be delayed until an incident, problem, or change has a significant business impact.|
    |Priority|Priority is based on impact and urgency, and it identifies how quickly the service desk should address the task.|
    |Application|Application scope of the rules. The scope defines whether the rules are available for all applications or for scoped applications.|
    |Active|Option to define whether the rule is active or not.|
    |Order|Sequence in which the rules appear in the priority lookup list. This field indicates the sequence of the rule that is executed first.|

    **Note:**

    Priority is calculated according to the following sample data lookup rules:

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

4.  Click **Submit**.


**Parent Topic:**[Configuring Incident Management](../concept/incident-configuration.md)

