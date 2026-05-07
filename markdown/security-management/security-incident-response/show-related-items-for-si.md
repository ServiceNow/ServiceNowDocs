---
title: View related items for a security incident
description: You can view related items, such as similar and child security incidents, related users, vulnerability groups, and vulnerable items associated with a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View related items for a security incident

You can view related items, such as similar and child security incidents, related users, vulnerability groups, and vulnerable items associated with a security incident.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open the security incident for which you want to view related items.

3.  Select the **Related Records** tab.

4.  Select any of the related lists to view or add information for the security incident.

<table id="table_hng_51r_yy"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child Security Incidents

</td><td>

The task record related to the issue that created the caused this security incident.

</td></tr><tr><td>

Similar Security Incidents

</td><td>

Other security incidents associated with any of the same observable records.The **Link as Children** button can be used to assign the selected similar security incidents as the children of the currently opened security incident.

</td></tr><tr><td>

Related Configuration Items

</td><td>

Displays a list of security incidents containing configuration items with the same observable as this security incident. This list can be filtered using the **CI exclusions** filter group. When an observable is added to a security incident this list is automatically updated. By default, observables with a context type of Destination are excluded.

</td></tr><tr><td>

Related Users

</td><td>

Displays a list of security incidents containing users with the same observables as this security incident. This list can be filtered using the **User exclusion** filter group. When an observable is added to a security incident this list is automatically updated. By default, observables with a context type of Destination are excluded.

</td></tr><tr><td>

Related Filter Group

</td><td>

After configuration items are identified, any matching CI or Filter group are automatically added.

</td></tr><tr><td>

Vulnerability Groups

</td><td>

If Vulnerability Response is activated, you can view vulnerability groups associated with this security incident.

</td></tr><tr><td>

Vulnerable Items

</td><td>

If Vulnerability Response is activated, you can view vulnerability items associated with this security incident.

</td></tr><tr><td>

Risks

</td><td>

If any of the core Risk Management plugins \(Policy and Compliance Management, Audit, Management, or Risk Management\) are activated, you can view or add risks associated with the security incident. This related list can be from the form header context menu under **Configure** &gt; **Related Lists**.

</td></tr><tr><td>

Configuration item events

</td><td>

Tab to view events, if Event Management is activated.

</td></tr><tr><td>

Configuration item alerts

</td><td>

Tab to view alerts, if Event Management is activated.

</td></tr><tr><td>

Customer Service Cases

</td><td>

Tab to view Customer Service case information, if Customer Service is activated.

</td></tr></tbody>
</table>5.  Select any of the following related links to further update the security incident:

    -   [Show Affected Items](show-affected-items-for-si.md)
    -   [Show IoC](show-ioc-info-for-si.md)
    -   [Show Enrichment Data](show-enrich-data-for-si.md)
    -   [Show Response Tasks](show-response-tasks-for-si.md)
6.  Select **Submit**.


