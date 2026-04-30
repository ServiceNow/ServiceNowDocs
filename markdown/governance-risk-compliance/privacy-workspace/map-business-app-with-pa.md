---
title: Map a table with a processing activity
description: Keep your processing activity updated and in sync with any table in ServiceNow by mapping the entity fields with the processing activity.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Map a table with a processing activity

Keep your processing activity updated and in sync with any table in ServiceNow® by mapping the entity fields with the processing activity.

## Before you begin

Role required: sn\_privacy.analyst

## About this task

A processing activity is associated with a CMDB table record such as a business process record or a business application record. Whenever a CMDB record is updated, the respective processing activity must also be updated so that the privacy teams can apply the controls based on the updates to the processing activity. Using the **Sync fields** button on the processing activity form the privacy managers and analysts can update the processing activity. The processing activity is updated based on the configurations available in the processing activity mapping.

When the **Sync fields** button is selected, only the fields that are mapped with the processing activity are updated.

When mapping a **Processing activity field** with a **Mapping field**, it is important to note that the following mapping combinations are supported:

-   String to String
-   Reference type to the same Reference type
-   True or False
-   Integer to Integer and String

Additionally, ensure that there is valid data for both the fields. For example, if there are filter conditions applied in the Processing activity field, these must match the filter conditions in the Mapping field.

## Procedure

1.  Navigate to **All** &gt; **Privacy Workspace** &gt; **Configure privacy management** &gt; **Processing activity mapping**.

2.  Click **New**.

3.  In the **Mapping table** field, select **Business Application**.

4.  In the **Description** field, provide a brief description of the table.

5.  Click **Save**.

    The Processing activity field mappings related list appears.

6.  Click the Processing activity field mappings related list.

    1.  Click **New**.

    2.  In the **Processing activity field**, select the field of the processing activity form that you want to map with the business application table field.

    3.  In the **Mapping field**, select the field of the business application table field that you want to map with the processing activity field.

    4.  Click **Save**.


## Result

The mapping is successfully created. The fields that are mapped will be populated in the processing activity form.

**Parent Topic:**[Configuring Privacy Management](../concept/configure-privacy-mgmt.md)

