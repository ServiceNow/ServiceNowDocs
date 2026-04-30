---
title: Rollup MITRE-ATT&amp;CK information using Threat Lookup results
description: If you have not enabled automatic rollup of MITRE-ATT&amp;CK information, you can do this manually.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Rollup MITRE-ATT&amp;CK information using Threat Lookup results

If you have not enabled automatic rollup of MITRE-ATT&amp;CK information, you can do this manually.

## Before you begin

Role required: sn\_si.analyst

## About this task

If you have enabled [automatic roll up of MITRE-ATT&amp;CK information from Threat Lookup results](configure-mitre-att-ck-properties.md) to security incident, then the information is automatically rolled up. If you have not enabled automatic rollup, you can do this manually.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to enrich with the MITRE-ATT&amp;CK information.

3.  Click **Show All Related Lists** and the **Threat Lookup Results** tab.

4.  Select the observable and then from the Actions menu, click **Roll up MITRE ATT&amp;CK Information to SI**.

    You can select multiple observables and rollup the information.

5.  Click **Reload** to confirm the changes.

    The following illustration shows how to select an observable and roll up the Threat Lookup results to the security incident.![Manually rollup threat lookup results.](../image/mitre-rollup-threat-lookup.gif)

    You can view the MITRE-ATT&amp;CK Card to confirm that the Threat Lookup results have been rolledup to the security incident.


**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](../concept/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](rollup-mitre-attack-information-detection-rules.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](rollup-mitre-att-ck-information-from-child-security-incidents.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](link-analysis-threat-hunt-mitre.md)

[MITRE-ATT&amp;CK heat map and navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#)

[Using the MITRE-ATT&amp;CK dashboard](../concept/mitre-dashboards.md#)

