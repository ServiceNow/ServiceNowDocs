---
title: Associate MITRE-ATT&amp;CK information with observables
description: Associate MITRE-ATT&amp;CK tactics and techniques to an observable for better security incident and threat analysis at a granular level.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Associate MITRE-ATT&amp;CK information with observables

Associate MITRE-ATT&amp;CK tactics and techniques to an observable for better security incident and threat analysis at a granular level.

## Before you begin

Role required: sn\_si.analyst

## About this task

Some SIEMs may provide MITRE-ATT&amp;CK information with events, alerts, or observables. To associate the MITRE-ATT&amp;CK information at a granular level, you can add the information with an observable.

You can choose to roll up the MITRE-ATT&amp;CK information automatically from the observables to a security incident. For automatic rollup of observables to security incidents, [enable the system property](configure-mitre-att-ck-properties.md). Alternatively, you can roll up the information manually for each observable.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to enrich with the MITRE-ATT&amp;CK information.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

4.  Point to the observable that you want to associate, right-click, and select **Associate MITRE ATT&amp;CK Technique**.

    In the following illustration, you can see how to navigate from the related list to **Associate MITRE ATT&amp;CK Technique**, review the source, and add a tactic and technique.

    ![Associate MITRE ATT&CK information with an observable.](../image/mitre-associate-observable.gif)

5.  In the source lists, review the **Source**.

    **Note:** Only the [collections](setup-mitre-profile.md) and [matrices](view-mitre-collection.md) that have been activated appear in the source list.

6.  Review the **Tactic** and **Techniques**, and add or remove them based on the relevance with the observable.

7.  Click **Save**.

    The tactics and techniques that you have added appear in the MITRE-ATT&amp;CK Information column in the observables related list.

8.  Select the observable and then from the Actions menu, click **Roll up MITRE ATT&amp;CK Information to SI**.

    If you have enabled [automatic roll up of MITRE-ATT&amp;CK information from observables to security incident](configure-mitre-att-ck-properties.md), then the information is automatically rolled up. If you have not enabled automatic rollup,you need to do this manually.

    The following illustration shows how to select an observable and roll up the MITRE-ATT&amp;CK information to a security incident.

    ![Manually roll up MITRE ATT&CK information from observable to security incident.](../image/mitre-manual-rollup.gif)

9.  To see an aggregated view of the techniques that are associated with the observables, select two or more observables from the list and then from the **Actions** menu on the selected rows list, click the **Show MITRE ATT&amp;CK Information**.


## Result

An aggregated view of the MITRE ATT&amp;CK information for the selected observables is displayed.

**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](../concept/mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](rollup-mitre-attack-information-detection-rules.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](rollup-mitre-att-ck-information-from-child-security-incidents.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](link-analysis-threat-hunt-mitre.md)

[MITRE-ATT&amp;CK heat map and navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#)

[Using the MITRE-ATT&amp;CK dashboard](../concept/mitre-dashboards.md#)

