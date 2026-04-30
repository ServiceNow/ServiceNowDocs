---
title: Security Incident Management Premium dashboard
description: This dashboard uses advanced Platform Analytics visualizations to aid security managers to track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery. The licensed version of Performance Analytics is therefore required.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Security Incident Response Platform Analytics Solutions, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Management Premium dashboard

This dashboard uses advanced Platform Analytics visualizations to aid security managers to track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery. The licensed version of Performance Analytics is therefore required.

![The Process by State tab of the Security Incident Management Premium dashboard](../../../product/security-incident-response/image/sec-incident-mgmt-premium.png "Security incident response by state")

![Workbench widget showing key security incident indicators broken down by age](../../../product/security-incident-response/image/si-mgmt-premium-age.png "Security incident response by age")

## End users and roles

|End user and goal|Required role|Benefits|
|-----------------|-------------|--------|
|Security Response Manager: Needs clear visibility into the overall state and volume of security incidents associated with applications and services.|sn\_si.manager|Can review the overall security posture with the ability to adjust the members of assignment groups.|
|Security Response Administrator: Needs to pinpoint areas of concern quickly and have full control over all Security Incident Response data while administering territories and skills, as needed.|sn\_si.admin|Can adjust risk calculation parameters to ensure vulnerable items that are most pertinent to the organization are being addressed first.|
|Security Response Analysts: Need to quickly prioritize which vulnerabilities to focus on based upon criticality to the organization.|sn\_si.analyst|Tier 1 and 2 security analysts work on security incidents. They can create and update security incidents, requests, and tasks, as well as problems, changes, and outages related to their incidents.|

## Security Incident Management Premium indicators

The Process by State and Process by Age tabs contain workbench widgets with the following indicators:

-   **Average age**

    The Average age of open security incidents indicator uses the formula `[[Summed age of open security incidents]] / [[Number of open security incidents]] / 24` to give a result in days.

-   **Average reassignment times**

    The Average re-assignment of open security incidents indicator uses the formula `Summed re-assignment of open security incidents / Number of open security incidents`.

-   **Average age of last update**

    The Average age of last update of open security incidents indicator uses the formula `Summed age of last update of open security incidents / Number of open security incidents / 24` to give a result in days.

-   **% not updated in 5 days**

    The % of open security incidents not updated in last 5 days indicator uses the formula `( [[Number of open security incidents not updated in the last 5 days]] / [[Number of open security incidents]] ) * 100`.


The Data Quality tab has interactive filters for the Category of the security incident and the levels of Risk, Priority, and Severity. These filters are applied simultaneously to the following indicators:

-   **Security Incidents Open for More Than 30 Days by Assignment Group and State**

    The Number of open security incidents filtered for an age of 30 days and broken down by Assignment group and State.

    ![Heatmap widget of security incidents open more than 30 days with the Assignment Group and State level 1 and 2 breakdowns](../../../product/security-incident-response/image/security-incident-open-30-days.png)

-   **Security Incidents With Assignee That is not Active**

    The Number of open security incidents with no assignee or an assignee who is not active.

-   **Security Incidents Open for More Than 30 Days by Assignment Group and State**

    The Number of open security incidents not updated in the last 30 days indicator broken down by Assignment group and State.


The KPI tab has the following additional indicators:

-   % of new critical security incidents
-   Average Age of Open Security Incidents
-   Average Close Time of Security Incidents
-   % Of Security Incidents that have been reassigned
-   % of Security Incidents closed on first assignment
-   % of security incidents closed by self-service
-   % of security incidents not solved
-   Average Close time of security incident tasks

## Breakdowns

The following breakdowns apply to the indicators on the dashboard:

-   Security Group
-   Security Incident Age
-   Security Incident Category
-   Security Incident Priority
-   Security Incident State

**Parent Topic:**[Security Incident Response Platform Analytics Solutions](security-incident-content-pack.md)

**Related topics**  


[CISO dashboard](ciso-dashboard.md)

[Security Incident Management dashboard](security-incident-mgmt-dashboard.md)

[Security Incident Explorer dashboard](si-explorer-dashboard.md)

[Security Operations Efficiency dashboard](../../../product/security-incident-response/concept/cj-sir-socpa-dashboard.md)

