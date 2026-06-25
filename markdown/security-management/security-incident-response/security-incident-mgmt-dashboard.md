---
title: Security Incident Management dashboard
description: With this dashboard, security managers can easily track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/security-incident-mgmt-dashboard.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Platform Analytics Solutions, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Management dashboard

With this dashboard, security managers can easily track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery.

\[Omitted image "si-mgmt-dashboard-overview.png"\] Alt text: Open security incidents and basic security indicators on the Security Incident Management dashboard

\[Omitted image "si-mgmt-dashboard-open.png"\] Alt text: Security Incident Management tab that shows open incidents

\[Omitted image "si-mgmt-dashboard-new.png"\] Alt text: Tab showing new security incidents

\[Omitted image "si-mgmt-dashboard-closed.png"\] Alt text: Tab showing number of closed incidents and average resolution time

\[Omitted image "si-mgmt-dashboard-daily.png"\] Alt text: Daily view of security incidents. Same format as 7-day and 28-day.

The **7d Running** and **28d Running** tabs follow the format of the **Daily** tab.

## End users and roles

|End user and goal|Required role|Benefits|
|-----------------|-------------|--------|
|Security Response Manager: Needs clear visibility into the overall state and volume of security incidents associated with applications and services.|sn\_si.manager|Can review the overall security posture with the ability to adjust the members of assignment groups.|
|Security Response Administrator: Needs to pinpoint areas of concern quickly and have full control over all Security Incident Response data while administering territories and skills, as needed.|sn\_si.admin|Can adjust risk calculation parameters to ensure vulnerable items that are most pertinent to the organization are being addressed first.|
|Security Response Analysts: Need to quickly prioritize which vulnerabilities to focus on based upon criticality to the organization.|sn\_si.analyst|Tier 1 and 2 security analysts work on security incidents. They can create and update security incidents, requests, and tasks, as well as problems, changes, and outages related to their incidents.|

## Security Incident Management indicators

The Security Incident Management dashboard presents the following key performance indicators:

-   **New Security Incidents**

    A chart of the number of new security incidents.

-   **Open Security Incidents**

    A chart where you can compare the number of open security incidents, the number of open security incidents not updated in the last 30 days, and the number of open security incidents not updated in the last 5 days.

-   **Basic Security Indicators**

    The last 6 days of scores of the number of new security incidents, the number of closed security incidents, the security incident backlog growth, and Number of open security incidents indicators.

-   **New Security Incidents by Priority**

    The number of new security incidents broken down by priority.


## Breakdowns

The following breakdowns apply to the indicators on the dashboard:

-   Security Group
-   Security Incident Age
-   Security Incident Category
-   Security Incident Priority
-   Security Incident State

**Parent Topic:**[Security Incident Response Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/security-incident-content-pack.md)

**Related topics**  


[CISO dashboard]()

[Security Incident Management Premium dashboard]()

[Security Incident Explorer dashboard]()

[Security Operations Efficiency dashboard]()

