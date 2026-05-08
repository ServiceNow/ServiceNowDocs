---
title: View enrichment data for a security incident
description: You can view enrichment data, such as running processes, running services, and network statistics associated with a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View enrichment data for a security incident

You can view enrichment data, such as running processes, running services, and network statistics associated with a security incident.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident for which you want to view enrichment data.

2.  Click the **Show Enrichment Data** related link.

3.  Click any of the related lists to view or add information for the security incident.

    **Note:** Raw data details are stored in an attachment to the enrichment data record. If they exceed the field limit, displayed details are truncated.

    |Tab|Description|
    |---|-----------|
    |Running Processes|Stores the records created by the Security Incident Response **Get Running Processes** workflow.|
    |Running Services|Stores the records created by the Security Incident Response **Get Running Services** workflow.|
    |Network Statistics|Stores the records created by the Security Incident Response **Get Network Statistics** workflow.|
    |Domain Lookups|If the WhoisXML API Integration plugin is activated, stores the records created by a Whois lookup.|
    |Firewall Logs|Stores enrichment data from firewall logs, such as the Palo Alto Network firewall logs.|
    |Compromised User Info|Stores accounts identified as being compromised through a Have I Been Pwned? lookup.|

    Note: The **Security Enrichment Data** tab shows raw enrichment data from Security Incident Response workflows, such as retrieving network statistics or running processes. This tab can be viewed by clicking the **Show All Related Lists** related link.

4.  Click any of the following related links to further update the security incident:

    -   [Show Affected Items](show-affected-items-for-si.md)
    -   [Show Related Items](show-related-items-for-si.md)
    -   [Show IoC](show-ioc-info-for-si.md)
    -   [Show Response Tasks](show-response-tasks-for-si.md)
5.  When you have completed your entries, click **Submit**.


