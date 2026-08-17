---
title: Bind CIs using CI field and column matching
description: Bind CIs by matching event Additional information fields with CI attributes. If column names differ, manually create an additional key-value pair to align with the CI table, ensuring accurate CI association.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/ci-matching-manual-field.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind CIs using CI field and column matching

Bind CIs by matching event **Additional information** fields with CI attributes. If column names differ, manually create an additional key-value pair to align with the CI table, ensuring accurate CI association.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

**Note:** Use [Enrich automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/enrich-alert-sow-itom.md) in Service Operations Workspace, the updated way to transform and standardize alert data for better response.

If no match is found using the **Node** field, the system looks at the **Additional information** field in the event record. There may be cases where no match is found because the column names in the event record and the table differ for the same item. In such cases, you can manually create an additional key-value pair with a name matching the table column and add it to the **Additional information** field, ensuring the matching process continues successfully.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and complete the required fields, or open an existing event rule record to modify it.

3.  Select the **Transform and Compose Alert Output** tab.

4.  Select the **Manual attributes** check box.

5.  In the **Field Name** and **Field Value** fields, enter the corresponding field name and specify the source field from which the value should be populated.

    \[Omitted image "em-ms-iis-webserver-attribute.png"\] Alt text: Manual attribute for an alert.

    Use the add icon \(\[Omitted image "em-add-icon.png"\] Alt text: Add icon\) icon to add multiple fields as needed.

6.  Select **Save**.

    The fields are created in the event rules record. However, when any alert is generated from an event using the event rule, the manually added fields appear in the **Additional information** field of the alert.


