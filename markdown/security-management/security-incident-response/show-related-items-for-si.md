---
title: View related items for a security incident
description: You can view related items, such as similar and child security incidents, related users, vulnerability groups, and vulnerable items associated with a security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View related items for a security incident

You can view related items, such as similar and child security incidents, related users, vulnerability groups, and vulnerable items associated with a security incident.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident for which you want to view related items.

2.  Click the **Show Related Items** related link.

3.  Click any of the related lists to view or add information for the security incident.

<table id="table_hng_51r_yy"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child Security Incidents

</td><td>

Select a task record related to the issue that caused this security incident to be created.

</td></tr><tr><td>

Similar Security Incidents

</td><td>

View any other security incidents associated with any of the same observable records.

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

If any of the core Risk Management plugins \(Policy and Compliance Management, Audit, Management, or Risk Management\) are activated, you can view or add risks associated with the security incident. You can add this related list from the form header context menu under **Configure** &gt; **Related Lists**.

</td></tr><tr><td>

Configuration item events

</td><td>

If Event Management is activated, you can view events.

</td></tr><tr><td>

Configuration item alerts

</td><td>

If Event Management is activated, you can view alerts.

</td></tr><tr><td>

Customer Service Cases

</td><td>

If Customer Service is activated, you can view Customer Service case information.

</td></tr></tbody>
</table>4.  Click any of the following related links to further update the security incident:

    -   [Show Affected Items](show-affected-items-for-si.md)
    -   [Show IoC](show-ioc-info-for-si.md)
    -   [Show Enrichment Data](show-enrich-data-for-si.md)
    -   [Show Response Tasks](show-response-tasks-for-si.md)
5.  When you have completed your entries, click **Submit**.


