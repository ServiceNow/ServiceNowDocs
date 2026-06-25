---
title: Rollup MITRE-ATT&amp;CK information from child security incidents
description: If you have not enabled automatic rollup of MITRE-ATT&amp;CK information, you can do this manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/rollup-mitre-att-ck-information-from-child-security-incidents.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Rollup MITRE-ATT&amp;CK information from child security incidents

If you have not enabled automatic rollup of MITRE-ATT&amp;CK information, you can do this manually.

## Before you begin

Role required: sn\_si.analyst

## About this task

If you have enabled [automatic roll up of MITRE-ATT&amp;CK information from child security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configure-mitre-att-ck-properties.md), then the information is automatically rolled up. If you have not enabled automatic rollup, you can do this manually.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the parent security incident that you want to enrich with the child MITRE-ATT&amp;CK information.

3.  Click **Show All Related Lists** and the **Child Security Incidents** tab.

4.  Select the child security incident and then from the Actions menu, click **Roll up MITRE ATT&amp;CK Information to SI**.

    You can click **Show MITRE ATT&amp;CK information** to view the child security incident's MITRE information before you roll up the MITRE ATT&amp;CK information.

5.  Click **Reload** to confirm the changes.

6.  Click the **MITRE ATT&amp;CK Card** to view the origin of techniques.

    The following illustration shows how to select child security incident and roll up the MITRE-ATT&amp;CK information to the parent security incident.\[Omitted image "mitre-rollup-information-child-si.gif"\] Alt text: This illustration shows how to roll up MITRE informtion from a child security incident to a parent security incident.

    You can view the MITRE-ATT&amp;CK Card to confirm that the child security incident MITRE-ATT&amp;CK information has been rolled up to the parent security incident.


**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents]()

[Associate MITRE-ATT&amp;CK information with observables]()

[Associate MITRE-ATT&amp;CK information with security case]()

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results]()

[Rollup MITRE-ATT&amp;CK information from detection rules]()

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters]()

[MITRE-ATT&amp;CK heat map and navigator]()

[Using the MITRE-ATT&amp;CK dashboard]()

