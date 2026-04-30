---
title: Operational Technology Action-Oriented Landing Page
description: You can use the Operational Technology \(OT\) Action-Oriented Landing Page to track critical tasks related to your OT network.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Explore, Industrial Workspace, Operational Technology]
---

# Operational Technology Action-Oriented Landing Page

You can use the Operational Technology \(OT\) Action-Oriented Landing Page to track critical tasks related to your OT network.

## OT Action-Oriented Landing Page overview

The OT Action-Oriented Landing Page helps users, such as OT engineers, view tasks assigned to them, their site, or their group. The landing page calls out important actions that must be prioritized for the signed-in user and includes an overview of existing OT incidents, OT change requests, OT remediation tasks, OT vulnerable items, and other tasks.

The landing page provides a detailed and role-based view of the daily tasks and important actions. Each task in the **Important Action** section shows tasks sorted by their **Opened** date by default. If the task is critical, then it shows up in the **Important Action** section.

To access the OT Action-Oriented Landing Page, navigate to **All** &gt; **Industrial Workspace**, select the Home \(![Home icon in the Industrial Workspace.](../../mftg-manufacturing-process-mgr/image/home-icon.png)\) icon.

## Landing page contents

The following sections describe the content that you can view in the OT Action-Oriented Landing Page.

**Important actions**

The Important actions section contains OT tasks or actions that are considered critical and must be addressed as soon as possible. By default, the tasks are organized by their **Opened** date with the most recently created critical task assigned to the signed in user shown first.

The tasks shown in this section are the most critical tasks pulled from the **Overview** section that you can act on. Task criticality is determined by the following criteria:

-   Their priority is critical
-   The task is a remediation task and its risk rating is critical

The tasks included in this section are organized in the following ways:

-   All tasks directly assigned to the signed in user are shown first.
-   Tasks assigned to a user's group that are also not assigned to any user are shown after.
-   Tasks that aren't assigned to a group or user but are assigned to a site the signed in user has access to are shown last.

**Overview**

The Overview section contains an overview of OT incidents, change requests, remediation tasks, vulnerable items, and other tasks assigned to you, your group, or your site.

You can use the following filters to view the records shown based on the **Assigned to**, **Assignment group**, and **Site** fields on the records:

-   **Your work**

    Records assigned to you.

-   **Your group's work**

    Records assigned to your group or groups.

-   **Your site's work**

    Records assigned to your site or sites.


The following table describes the tiles in the Overview section.

<table id="id_n1t_2cd_1cc"><thead><tr><th>

Tile

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Incidents assigned to you / OT Incidents assigned to your groups / OT Incidents assigned to your sites

</td><td>

Number of OT incident records assigned to either you, your assignment group, or your site.To view a list of all the OT incident records, select **All records**.

To only show the list of records based on their state or type, select the respective section of the available graph. For example, if you only want to view the incident records based on their priority, select the **Critical** section of the graph.

</td></tr><tr><td>

OT Change Requests assigned to you / OT Change Requests assigned to your groups / OT Change Requests assigned to your sites

</td><td>

Number of OT change request records assigned to either you, your assignment group, or your site.To view a list of all the OT change request records, select **All records**.

To only show the list of records based on their state, select the respective section of the available graph. For example, if you only want to view the change request records that are scheduled, select the **Scheduled** section of the graph.

</td></tr><tr><td>

OT Remediation Tasks assigned to you / OT Remediation Tasks assigned to your groups / OT Remediation Tasks assigned to your sites

</td><td>

Number of OT remediation task records assigned to either you, your assignment group, or your site.To view a list of all the OT remediation task records, select **All records**.

To only show the list of records based on their state, select the respective section of the available graph. For example, if you only want to view the remediation task records that are in review, select the **In Review** section of the graph.

</td></tr><tr><td>

OT Vulnerable Items assigned to you / OT Vulnerable Items assigned to your groups / OT Vulnerable Items assigned to your sites

</td><td>

Number of OT vulnerable item records assigned to either you, your assignment group, or your site.To view a list of all the OT vulnerable item records, select **All records**.

To only show the list of records based on their risk rating, select the respective section of the available graph. For example, if you only want to view the vulnerable item records that are a high priority, select the **High** section of the graph.

</td></tr><tr><td>

Other OT Tasks assigned to you / Other OT Tasks assigned to your groups / Other OT Tasks assigned to your sites

</td><td>

Number of other OT task records assigned to either you, your assignment group, or your site.To view a list of all the other OT task records, select **All records**.

To only show the list of records based on their priority, select the respective section of the available graph. For example, if you only want to view the OT tasks that are considered low priority, select the low section of the graph.

</td></tr></tbody>
</table>**OT CMDB Health**

The OT CMDB Health helps you monitor and maintain the health of your devices in the Configuration Management Database \(CMDB\). You can view the number of your OT devices organized by type.

**Note:** This section is only displayed if you have Operational Technology Manager installed.

The following table describes the tiles in the OT CMDB Health section. To view the OT CMDB Health section, you must have the **cmdb\_ot\_isa\_viewer** role.

<table id="table_bns_jsj_r1c"><thead><tr><th>

Tile

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unclassed OT devices

</td><td>

Number of the OT devices in your OT network that aren't assigned an OT device type category.To view the list of unclassed OT device records, select **All records**.

</td></tr><tr><td>

Unassigned OT devices

</td><td>

Number of the OT devices in your OT network that aren't assigned to a user.To view the list of unassigned OT device records, select **All records**.

</td></tr><tr><td>

Unmapped OT devices

</td><td>

Number of the OT devices in your OT network that aren’t mapped to any equipment model entity for your assigned site.To view the list of unmapped OT device records, select **All records**.

**Note:** This tile is only available when the Industrial Process Manager is installed and if the signed in user has the cmdb\_ot\_isa\_viewer role. The tile requires that your organization has an equipment model for mapping OT devices to a production process.

</td></tr><tr><td>

No site assigned

</td><td>

Number of OT devices in your OT network that aren't assigned to a site.**Note:** This tile is only available if the signed in user has the cmdb\_ot\_isa\_viewer role.

To view the list of OT device records without a site, select **All records**.

</td></tr><tr><td>

No IP address OT devices

</td><td>

Number of OT devices in your OT network that aren't assigned an IP address.To view the list of OT device records without an IP address, select **All records**.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring the Industrial Workspace](exploring-industrial-workspace.md)

