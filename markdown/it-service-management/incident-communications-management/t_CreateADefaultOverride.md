---
title: Create a default override
description: Create a default override to specify the user or group for a contact definition in an incident communication plan. Use multiple conditions to determine which user or group becomes the contact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/t\_CreateADefaultOverride.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management and contacts, Managing incident communications, Incident Communications Management, IT Service Management]
---

# Create a default override

Create a default override to specify the user or group for a contact definition in an incident communication plan. Use multiple conditions to determine which user or group becomes the contact.

## Before you begin

Role required: ia\_admin or admin

## About this task

The Default overrides related list is available only if you select **Default Override** as the value of the **Source** field in the Contact definition form.

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Contact Administration** &gt; **Contact Definitions**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open the contact definition record.

3.  In the Default overrides related list, select **New**.

    \[Omitted image "NewDefaultOverride.png"\] Alt text: Default override form

4.  On the form, fill in the fields.

<table id="table_wf5_bzg_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order

</td><td>

Order in which the default override condition is evaluated.

</td></tr><tr><td>

User value

</td><td>

User assigned as the contact when the default override condition matches. **Note:** The **User value** field appears if the value of the **Type** field in the Contact definition form is **User**.

</td></tr><tr><td>

Group value

</td><td>

Group assigned as the contact when the default override condition matches. **Note:** The **Group value** field appears if the value of the **Type** field in the Contact definition form is **Group**.

</td></tr><tr><td>

Condition

</td><td>

Conditions that determine whether the default override values are applied. If multiple conditions are defined, they're evaluated in the listed order. If no conditions match, the default override is not applied.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Default override and its conditions are defined for a contact definition.


**Parent Topic:**[Incident Communications Management and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/c_IncidentAlertContact.md)

**Related topics**  


[Contact responsibilities for incident communication plans]()

[Define contact responsibilities]()

[Create a contact definition]()

[Add a user as a contact]()

