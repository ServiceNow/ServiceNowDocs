---
title: Associate MITRE Techniques to a Case
description: Associate one or more MITRE technique to a case.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating cases using Threat Analyst Workbench, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Associate MITRE Techniques to a Case

Associate one or more MITRE technique to a case.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Select any case.

5.  Click **Associate MITRE Technique** button.

6.  Click **Add Matrix** to associate the MITRE technique.

    The **Associate MITRE Technique to Case** dialogue box is displayed.

7.  Select the **Matrix**.

    All the enabled matrices will be displayed for you to select the Matrix.

8.  Select the tactic from the drop-down lists.

    All the tactics associated to a matrix will be displayed.

    **Note:** In case if you would want to add more tactics then click **Add Tactic**. The previously selected tactics will no longer be displayed in the drop-down list if you are adding a new tactic.

9.  Select the **Technique**.

    All the techniques associated to your selected tactic will be displayed. In case if you are adding more tactics then you can select the associated techniques for that selected tactics.

10. Click **Save**.

    If you want to delete the entire matrix associated data then click on **Delete Matrix**, this action will only remove the associated matrix data but the matrix will remain in the MITRE ATT&amp;CK Repository.

    The associated matrix data record is displayed under the MITRE ATT&amp;CK Card section. In the card view:

    **Note:** You can toggle between multiple matrices from the Matrix drop-down list.

    1.  The first row of the card view displays all the tactics associated to the current selected matrix.
    2.  Each tactic card shows the tactic name and number of techniques of that tactic mapped to the current case record.
    3.  All the associated techniques to that case are vertically showed under each tactic. You can click on any technique to view the technique form view.
11. Click **Show ID** will show the IDs for all the associated techniques.

    **Note:** Each technique card shows the technique name and technique ID only when **Show ID** is enabled.

12. Click **Refresh** to refresh the card view.

    You can view the time stamp of the last refresh for the selected matrix.

    **Note:** Click pop out icon to pop out the associated matrix card to view in a new tab.


**Parent Topic:**[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

