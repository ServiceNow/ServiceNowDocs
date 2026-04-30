---
title: Roll up of MITRE technique associations
description: Roll up of MITRE technique associations from observables, indicators, objects, and security incidents which are linked or unlinked from a case record.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-11-04"
reading_time_minutes: 2
breadcrumb: [Creating cases using Threat Analyst Workbench, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Roll up of MITRE technique associations

Roll up of MITRE technique associations from observables, indicators, objects, and security incidents which are linked or unlinked from a case record.

## Before you begin

**Note:**

-   Roll up of MITRE technique associations for security incidents will roll up the MITRE technique associated data from security incidents to the case management in TISC.
-   By default this property sn\_sec\_tisc.auto\_rollup\_mitre\_data is enabled for the MITRE Technique\(s\), to be rolled up to case\(s\) from the associated objects or security incidents automatically.
-   If you want to perform on demand roll up of MITRE technique associations then navigate to the more actions within the **Case form view** and select **Roll Up MITRE Techniques** option. This operation will happen asynchronously and you can verify the **Activity Stream** section for the updates on the roll up activity.

Role required: sn\_sec\_tisc.analyst

## About this task

-   Whenever any entity such as an observable or indicator is linked to any case, then all the MITRE technique associations that are present for that entity are automatically rolled up to the case.
-   Whenever any entity such as an observable or indicator is unlinked and removed from the case, then all the MITRE technique associations which are rolled up from the case that are present for that entity will be removed automatically and rolled up to the case.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Open any case.

5.  Go to **Artifacts** tab.

6.  Select **Observables** from the artifacts related list.

7.  Select the **Link** button.

8.  Select the observables that you may want to link to the case.

9.  Click **Link** to link the observables.

    After you link the observables to a case then the MITRE techniques associated for that particular observable are automatically rolled up and the MITRE techniques list count under the artifacts section is automatically updated.

10. Click **Unlink** to unlink the observables from the case.

    After you unlink the observables to a case then the MITRE techniques associated for that particular observable are automatically removed and the MITRE techniques list count under the artifacts section is automatically updated.


**Parent Topic:**[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

