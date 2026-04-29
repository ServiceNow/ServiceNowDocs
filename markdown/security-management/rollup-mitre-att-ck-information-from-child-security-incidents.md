---
title: Rollup MITRE-ATT&amp;CK information from child security incidents
description: If you have not enabled automatic rollup of MITRE-ATT&amp;CK information, you can do this manually.
locale: en-US
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

If you have enabled [automatic roll up of MITRE-ATT&amp;CK information from child security incidents](configure-mitre-att-ck-properties.md), then the information is automatically rolled up. If you have not enabled automatic rollup, you can do this manually.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the parent security incident that you want to enrich with the child MITRE-ATT&amp;CK information.

3.  Click **Show All Related Lists** and the **Child Security Incidents** tab.

4.  Select the child security incident and then from the Actions menu, click **Roll up MITRE ATT&amp;CK Information to SI**.

    You can click **Show MITRE ATT&amp;CK information** to view the child security incident's MITRE information before you roll up the MITRE ATT&amp;CK information.

5.  Click **Reload** to confirm the changes.

6.  Click the **MITRE ATT&amp;CK Card** to view the origin of techniques.

    The following illustration shows how to select child security incident and roll up the MITRE-ATT&amp;CK information to the parent security incident.![This illustration shows how to roll up MITRE informtion from a child security incident to a parent security incident.](../image/mitre-rollup-information-child-si.gif)

    You can view the MITRE-ATT&amp;CK Card to confirm that the child security incident MITRE-ATT&amp;CK information has been rolled up to the parent security incident.


**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](../concept/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](rollup-mitre-attack-information-detection-rules.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](link-analysis-threat-hunt-mitre.md)

[MITRE-ATT&amp;CK heat map and navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#)

[Using the MITRE-ATT&amp;CK dashboard](../concept/mitre-dashboards.md#)

