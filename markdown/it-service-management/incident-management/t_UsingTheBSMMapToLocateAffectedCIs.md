---
title: View affected CIs in the dependency views map
description: A configuration item \(CI\) can result in an incident. Use dependency view to identify other configuration items \(CIs\) that are affected by the CI that resulted in the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/t\_UsingTheBSMMapToLocateAffectedCIs.html
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

<table id="choicetable_crl_z1k_yy"><thead><tr><th align="left" id="d260603e71">

From where

</th><th align="left" id="d260603e74">

Action

</th></tr></thead><tbody><tr><td id="d260603e80">

**Configuration item field**

</td><td>

Click the lookup icon \(\[Omitted image "look-up-icon.png"\] Alt text: The Look up icon\) beside the field and select the CI.

</td></tr><tr><td id="d260603e95">

**Affected CIs related list**

</td><td>

1.  Select **Add** at the top of the list.
2.  Select the CI to associate.
3.  Select **Add Selected**.
4.  Right-click on the form header and then select **Save**.


</td></tr></tbody>
</table>2.  Select the dependency views icon \(\[Omitted image "BusinessServiceMapIcon.png"\] Alt text: Dependency views icon\) beside the **Configuration item** field.

    The Dependency Views map opens in a new tab or window.

3.  To see items that this CI affects, select the down arrow and then select **View Affected CIs**.

    \[Omitted image "IM\_CIOptionsDepViews.png"\] Alt text: Select the View affected CIs option from the menu

    To add another affected CI to the incident, select the down arrow beside the CI and then select **Add Affected CI\(s\)**.


**Related topics**  


[Dependency Views map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/dependency-views/c_NextGenBSMMaps.md)

