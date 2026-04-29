---
title: Show MITRE ATT&amp;CK Framework for a Case\(s\)
description: Displays all the associated techniques of a case on the MITRE ATT&amp;CK framework.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add artifacts to case\(s\) or case task\(s\), Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Show MITRE ATT&amp;CK Framework for a Case\(s\)

Displays all the associated techniques of a case on the MITRE ATT&amp;CK framework.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Select the required MITRE ATT&amp;CK matrix from the **Matrix** drop-down list. The MITRE ATT&amp;CK Framework shows different levels of tactics and techniques association.

1.  The top row displays all the tactics that are present in the selected **Matrix**. By default, all the tactics display the count of the total techniques and sub-techniques present for that corresponding tactics. You can use the **Refresh** icon to reload the MITRE ATT&amp;CK framework and view the latest associations.
2.  Under each tactic, the framework displays all the techniques that are present as a relationship to that corresponding tactic.
3.  The framework displays the sub-techniques that are present under each technique. Expand each technique to view the sub-techniques.

**Important:** In the framework, the techniques and sub-techniques that are associated with a case are highlighted.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Select any case.

5.  Go to **Artifacts** tab.

    The associated artifacts are displayed as the related lists for that specific case.

6.  Select **Show MITRE ATT&amp;CK Framework** button

    When you select this button, the framework displays all the associated techniques of a case and artifacts on the MITRE ATT&amp;CK.

7.  View MITRE ATT&amp;CK techniques and sub-techniques related to the case from the MITRE techniques that you have selected to view.

8.  Select any record to view the MITRE ATT&amp;CK techniques and sub-techniques related to the case.

9.  Use **View Controls** to view the MITRE ATT&amp;CK techniques and sub-techniques as desired.

    From the controls lists:

    -   Select **Show ID** to view the techniques and sub-techniques MITRE IDs.
    -   Select **Show Sub Techniques** to view all the sub-techniques. When you select this option, all the techniques are shown in the expanded view. The expanded view of the technique shows all the sub-techniques that are present for that corresponding technique.
    -   Select **Show Only Associated Techniques** to view only MITRE techniques that are associated with a case. When you select this option, each tactic shows the total number of associated techniques and sub-techniques.

**Parent Topic:**[Add artifacts to case\(s\) or case task\(s\)](add-artifacts-to-a-case-s.md)

