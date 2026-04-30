---
title: View affected CIs in the dependency views map
description: A configuration item \(CI\) can result in an incident. Use dependency view to identify other configuration items \(CIs\) that are affected by the CI that resulted in the incident.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# View affected CIs in the dependency views map

A configuration item \(CI\) can result in an incident. Use dependency view to identify other configuration items \(CIs\) that are affected by the CI that resulted in the incident.

## Before you begin

Role required: Itil, itil\_admin sn\_incident\_write, or admin

## About this task

Often, an incident is related to one or more specific configuration items \(CIs\). If the configuration management database \(CMDB\) is populated, the CI records hold valuable information to help resolve incidents. You can associate configuration items to an incident to see how the incident affects dependent CIs.

Use the **Configuration Item** field when a single CI is the cause of the incident and use the **Affected CIs** related list when multiple CIs are affected by the incident. For example, suppose a load-balancer in a data center is no longer operational. The **Configuration Item** field lists the specific server which is out of memory. The **Affected CI** related list contains the load-balancer, the data center, the servers that depend on the load-balancer, and business services that are impacted by the missing server.

## Procedure

1.  On the Incident form, associate the CIs.

<table id="choicetable_crl_z1k_yy"><thead><tr><th align="left" id="d266940e71">

From where

</th><th align="left" id="d266940e74">

Action

</th></tr></thead><tbody><tr><td id="d266940e80">

**Configuration item field**

</td><td>

Click the lookup icon \(![The Look up icon](../../itsm-workspace/image/look-up-icon.png)\) beside the field and select the CI.

</td></tr><tr><td id="d266940e95">

**Affected CIs related list**

</td><td>

1.  Select **Add** at the top of the list.
2.  Select the CI to associate.
3.  Select **Add Selected**.
4.  Right-click on the form header and then select **Save**.


</td></tr></tbody>
</table>2.  Select the dependency views icon \(![Dependency views icon](../image/BusinessServiceMapIcon.png)\) beside the **Configuration item** field.

    The Dependency Views map opens in a new tab or window.

3.  To see items that this CI affects, select the down arrow and then select **View Affected CIs**.

    ![Select the View affected CIs option from the menu](../image/IM_CIOptionsDepViews.png)

    To add another affected CI to the incident, select the down arrow beside the CI and then select **Add Affected CI\(s\)**.


**Related topics**  


[Dependency Views map](https://www.servicenow.com/docs/access?context=c_NextGenBSMMaps&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

