---
title: Configure settings to manage APIs in API Insights
description: Configure API Insights settings, including API creation tools, relationship models, ownership groups, and automated workflows, to streamline API governance and operational processes.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB administrator tasks, Configure, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure settings to manage APIs in API Insights

Configure API Insights settings, including API creation tools, relationship models, ownership groups, and automated workflows, to streamline API governance and operational processes.

## Before you begin

Role required: sn\_api\_insights\_ws.api\_mgmt\_architect\_adminor sn\_cmdb\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **Settings** tab.

3.  Turn on the All settings option.

    **Note:** This step is applicable to users with the sn\_cmdb\_admin role. You can skip this step if you have the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role.

4.  In the API creation tool section, select an API creation tool from the available options.

<table id="choicetable_mvn_tgd_ncc"><tbody><tr><td id="d74013e104">

**None**

</td><td>

Uses no external tool.

</td></tr><tr><td id="d74013e113">

**Digital Integration Management**

</td><td>

Uses the Digital Integration Management application \(part of the Enterprise Architecture Workspace\), if enabled, to initiate the API design process by creating a digital interface record.

</td></tr><tr><td id="d74013e125">

**External tool**

</td><td>

Uses a third-party tool for API creation, requiring the URL for the external tool \(for example, `http://www.postman.com` \) to be entered in the **External API authoring tool URL** field.

</td></tr></tbody>
</table>5.  In the API-to-business application relationship model section, select a relationship model from the available options.

    |Option|Description|
    |------|-----------|
    |**CSDM**|Links an API to an application service and then to business context also called as business application using the Common Service Data Model \(CSDM\).|
    |**Digital Integration Management**|Links an API to a digital interface and then to business context.|

6.  In the Ownership group section, set the ownership group responsible for managing the API.

<table id="choicetable_ots_vkd_ncc"><thead><tr><th align="left" id="d74013e198">

Option

</th><th align="left" id="d74013e201">

Description

</th></tr></thead><tbody><tr><td id="d74013e207">

**Managed by Group**

</td><td>

Assigns the API to a specific group responsible for its overall management and governance ensuring the API’s functionality, security, and alignment with business objectives.**Note:**

By default, the **SyncOwnershipGroupsOfAPIVersions** scheduled job is active, ensuring that the managed by group is synced for the next API version.

</td></tr><tr><td id="d74013e224">

**Change Group**

</td><td>

Assigns the API to a group that oversees changes, managing the life cycle to ensure modifications are documented and implemented without disrupting services.

</td></tr><tr><td id="d74013e233">

**Approval Group**

</td><td>

Assigns the API to a group handling approvals for actions like changes or deployments, ensuring necessary approvals are secured.

</td></tr><tr><td id="d74013e242">

**Support Group**

</td><td>

Assigns the API to a support group responsible for resolving incidents, maintaining stability, and troubleshooting issues.

</td></tr></tbody>
</table>7.  In the Configure workflows section, select a workflow for automating an API action.

    **Note:** Workflows are created by your administrator using the Workflow Studio. See [Configuring flows for API actions in API Insights](../concept/api-insights-workflow.md).

8.  Select **Save**.


