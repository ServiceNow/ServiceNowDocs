---
title: Associate MITRE Techniques to a Case
description: Associate one or more MITRE technique to a case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-associate-mitre-technique.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating cases using Threat Analyst Workbench, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Associate MITRE Techniques to a Case

Associate one or more MITRE technique to a case.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Analyst Workbench**.

2.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

3.  Select any case.

4.  Select **Associate MITRE Technique** button.

5.  Select **Add Matrix** to associate the MITRE technique.

    The **Associate MITRE Technique to Case** dialogue box is displayed.

6.  Select the **Matrix**.

    All the enabled matrices will be displayed for you to select the Matrix.

    **Note:**

    Each matrix in the list includes the MITRE ATT&amp;CK collection version that it was ingested from, for example Enterprise ATT&amp;CK \(v18.0\).

7.  Select the tactic from the drop-down lists.

    All the tactics associated to a matrix will be displayed.

    **Note:** In case if you would want to add more tactics then select **Add Tactic**. The previously selected tactics will no longer be displayed in the drop-down list if you're adding a new tactic.

8.  Select the **Technique**.

    All the techniques associated to your selected tactic will be displayed. In case if you're adding more tactics then you can select the associated techniques for that selected tactics.

    **Note:**

    Only the tactic and technique pairs that MITRE currently maps are offered, so you can't associate a pair that MITRE has stopped mapping. For more information, see [Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md).

9.  Select **Save**.

    If you want to delete the entire matrix associated data then select **Delete Matrix**, this action will only remove the associated matrix data but the matrix will remain in the MITRE ATT&amp;CK Repository.

    The associated matrix data record is displayed under the MITRE ATT&amp;CK Card section. In the card view:

    **Note:** You can toggle between multiple matrices from the Matrix drop-down list.

    1.  The first row of the card view displays all the tactics associated to the current selected matrix.
    2.  Each tactic card shows the tactic name and number of techniques of that tactic mapped to the current case record.
    3.  All the associated techniques to that case are vertically showed under each tactic. You can click on any technique to view the technique form view.
10. Select **Show ID** will show the IDs for all the associated techniques.

    **Note:** Each technique card shows the technique name and technique ID only when **Show ID** is enabled.

11. Select **Refresh** to refresh the card view.

    You can view the time stamp of the last refresh for the selected matrix.

    **Note:** Select pop out icon to pop out the associated matrix card to view in a new tab.


**Parent Topic:**[Creating cases using Threat Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/create-cases-using-threat-analyst-workbench.md)

