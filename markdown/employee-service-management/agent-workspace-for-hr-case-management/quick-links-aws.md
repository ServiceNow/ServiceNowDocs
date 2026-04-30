---
title: Configure quick links in Agent Workspace for HR Case Management
description: Configure quick links to quickly access internal and external resources related to specific departments within your organization.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [UI Builder for Agent Workspace for HR Case Management, Setting up Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Configure quick links in Agent Workspace for HR Case Management

Configure quick links to quickly access internal and external resources related to specific departments within your organization.

## Before you begin

Employee Center Pro must be installed. For more information, see [Install Employee Center Pro](../../employee-center/task/install-ec-pro.md).

Role required: sn\_hr\_agent\_ws.admin and sn\_hr\_core.basic

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Re-usable Components** &gt; **Link Content**.

2.  Create the link.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_whk_klc_rzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the link to content.**Note:** Ensure that you have content created in **Content Publishing** &gt; **Content Library** &gt; **View All**.

</td></tr><tr><td>

Type

</td><td>

The type of content, which for a quick link is **Link**.

</td></tr><tr><td>

URL

</td><td>

The URL link to the content to appear on the service portal.

</td></tr></tbody>
</table>    3.  For the **Load link in** field, select **Current page** to load the link in the current portal page.

    4.  Select **Submit**.

3.  Define when and where you want your content to be available.

    1.  Navigate to **All** &gt; **Content Publishing** &gt; **Schedule Content**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_ug2_dpc_rzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content

</td><td>

The content or information you want to make available as set in the link definition.

</td></tr><tr><td>

Active

</td><td>

Option to enable the form.

</td></tr><tr><td>

Title

</td><td>

Name of the schedule content record.

</td></tr><tr><td>

Audience

</td><td>

Audience for the content.

</td></tr><tr><td>

Content location

</td><td>

Location where the content you’re scheduling appears.

</td></tr><tr><td>

Approvers

</td><td>

Users who can approve the content before it’s made available.

</td></tr><tr><td>

Component type

</td><td>

Should be set to **Quick links**.

</td></tr><tr><td>

Availability start date

</td><td>

Date the content should first be available to the audience.

</td></tr><tr><td>

Availability end date

</td><td>

Final date the content is valid.

</td></tr></tbody>
</table>    4.  Enter or verify the field values in the following table.

        |Field|Value|
        |-----|-----|
        |Content|The newly created record|
        |Content location|UIB Workspace|
        |Component type|Quick links|

    5.  Select **Submit**.

4.  Map the link created above to the Quick link component in UI Builder.

    1.  Navigate to **All** &gt; **HR Case Management** &gt; **UI Builder for Agent Workspace for HR Case Management**.

    2.  Select **Landing page default** if you have not configured a landing page variant.

    3.  Select your landing page variant.

    4.  In the left pane, select the data icon \(![Data icon](../image/data-icon.png)\).![Data tab](../image/data-icon-aws.png)

    5.  Select **getQuickLinksContent**.![Get quick links panel](../image/get-quick-links.png)

    6.  In the **content\_id** field, enter the name given to the Content group.

    7.  Select **Save**.


**Parent Topic:**[UI Builder for Agent Workspace for HR Case Management](../concept/uib-aws.md)

**Related topics**  


[Create a landing page variant](configure-report-aws.md)

[Enable a detailed data display within a report](drill-down-report.md)

[Configure contextual side panel tabs in Agent Workspace for HR Case Management](configure-side-panel.md)

