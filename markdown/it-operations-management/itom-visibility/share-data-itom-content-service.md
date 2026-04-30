---
title: Share data on ITOM Content Service
description: Control data sharing by opting in or out of ITOM Content Service sharing options using the Discovery Admin Workspace.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-11-09"
reading_time_minutes: 2
keywords: [Discovery, Content, Service, Patterns]
breadcrumb: [ITOM Content Service, ITOM Visibility, IT Operations Management]
---

# Share data on ITOM Content Service

Control data sharing by opting in or out of ITOM Content Service sharing options using the Discovery Admin Workspace.

## Before you begin

Ensure that the following application and plugin are installed:

-   ITOM Content Service \(sn\_smart\_content\)
-   Discovery Admin Workspace \(com.snc.itom.daw\)

To share Service Info, confirm that ITOM Content Service and Discovery Admin Workspace are upgraded to the latest version.

-   ITOM Content Service \(at least version 1.6.2\)
-   Discovery Admin Workspace \(at least version 1.11.0\)

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace**.

2.  Indicate whether and what data you want to share with AI librarians.

<table id="choicetable_fch_mpt_c1c"><thead><tr><th align="left" id="d114109e124">

Option

</th><th align="left" id="d114109e127">

Actions

</th></tr></thead><tbody><tr><td id="d114109e133">

**Opt in to share your data**

</td><td>

1.  In the **Content service setup** tile, select **Opt in**.
2.  Read the agreement and select **Yes, I have read and agree with the Opt-in Agreement**.
3.  Select **Next**.
4.  Select your setup.
    -   Advanced - Activates a comprehensive set of classifiers for expanded visibility
    -   Basic - Activates the most common classifiers.
    -   Custom - You select which classifiers to activate.
5.  Turn on the data sharing options that you want to use.
    -   Running process fingerprint data: Shares metadata and some samples of processes from the Process Groups table.
    -   SNMP System OIDs: Shares metadata and some samples of processes from the SNMP OID table.
    -   Service Info: Shares metadata and some samples of processes from the Application Service Candidate table.
6.  Select **Save**.

7.  When the Opt-in is complete, select **Home** to return to the workspace.

The **Content service suggestions** tile replaces the **Content service setup** tile. In the new **Content service setup** section, a green check-mark appears indicating that you have opted in to ITOM Content Service.

</td></tr><tr><td id="d114109e236">

**Set the data sharing permissions off**

</td><td>

1.  In the **Content service setup** section, select **Configure setup**.
2.  Turn off one option or both options.
3.  Select **Save**.
4.  When the setting is complete, select **Home** to return to the workspace.


</td></tr><tr><td id="d114109e281">

**Opt out of sharing your data**

</td><td>

1.  In the **Content service setup** section, select **Opt out**.
2.  Select **Opt out**.
3.  Read the **Opting out of ITOM Content Service** system message and select **Opt out**.
4.  When the opt-out process is complete, select **Home** to return to the workspace.

ITOM Content Service stops using your data and your workspace presents only CIs defined by you. For more information, see [Discovery Admin Workspace](../concept/discovery-admin-workspace.md).

</td></tr></tbody>
</table>
**Related topics**  


[ITOM Content Service](../concept/discovery-content-services.md)

