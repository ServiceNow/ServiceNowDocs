---
title: Perform lookups on observables
description: You can perform threat intelligence lookups on one or more observables to determine whether they’re associated with known security threats. The scanning implementations that run depend on the ones you’ve activated.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Observables, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Perform lookups on observables

You can perform threat intelligence lookups on one or more observables to determine whether they’re associated with known security threats. The scanning implementations that run depend on the ones you’ve activated.

## Before you begin

Before you can perform lookups, you must activate the Threat Intelligence plugin. You must also install the plugin for one or more of the scanning implementations:

-   [CrowdStrike Falcon Intelligence integration](../../secops-integration-threat/secops-integration-crowdstrike-falcon-intell/reference/crowdstrike-intell-landing-page.md)
-   [OPSWAT Metadefender](../../secops-integration-threat/secops-integration-opswat-metadefender/concept/c_Metadefenderintegration.md#)
-   [Security Operations Have I been pwned?](../../secops-integration-sir/secops-integration-haveibeenpwned/task/activate-haveibeenpwned.md)
-   [VirusTotal](../../secops-integration-threat/secops-integration-virustotal/task/activate-configure-virustotal.md)

Role required: sn\_ti.write

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Observables**.

2.  Do one of the following steps:

    -   To perform a lookup on more than one observable, select the observables, click **Actions on selected rows**, and select **Run threat lookup**.
    -   To perform a lookup on a single observable, open the observable record, and click the **Run threat lookup** related link.
    ![Run Threat Lookup slushbucket](../image/run-threat-lookup.png)

3.  Select the threat lookup implementations you want to use, or select **All** to perform lookups using all of the active implementations, then click **Submit**.

    A message indicates that the threat lookups have begun. The [Security Operations Integration - Threat Lookup Flow](../../security-operations-integrations/task/sec-ops-integ-threat-lookup.md) runs and also executes the implementation workflows for the threat lookup implementations you selected. The lookups are performed and the results are generated.

4.  When the lookups are completed, you can click the **Threat Lookup Results** tab to view the results.

    ![Threat Lookup Results](../image/threat-lookup-results.png)

    **Recent Threat Lookup Result**: You can also see the latest or recent threat lookup results from each integration vendor when you click the **Recent Threat Lookup Result** tab.

    **Note:** The **Recent Threat Lookup Result** tab is not a part of the base system.

    To enable this tab, perform the following:

    1.  Right-click on the form header.

    2.  Navigate to **Configure** &gt; **Related Lists**.

    3.  Locate **Recent Threat Lookup Results** on the Available list and move it to the Selected list.

    4.  Click **Save**.

        You can now view the recent threat lookup results from each integration vendor in the **Recent Threat Lookup Result** tab.

        ![Recent Threat Lookup Result](../image/recent-threat-lookup-results.gif)

5.  To see additional details, including raw results for a specific lookup, click the **Result value**.

    **Note:** When the VirusTotal or OPSWAT Metadefender implementations are used, the details are consolidated, as shown below.

    ![Threat Lookup Results details](../image/threat-lookup-results-details.png)


**Parent Topic:**[Observables](../concept/c_Observables.md)

**Related topics**  


[Define an observable](t_AddObservable.md)

[Add a related IoC to an observable](t_AddIoCToObserv.md)

[Add associated tasks to an observable](t_AddAssociatedTasksToObservable.md)

[Add a related observable](t_AddRelatedObservable.md)

[Load more IoC data](t_LoadAdditionalIoCData.md)

[Identify observable sources](t_IdentifyObservbleSources.md)

[Perform threat enrichment on observables](perform-enrich-on-observs.md)

