---
title: Explore Access management console
description: Use the Access Management Console within Security Center to review and remediate access issues and misconfigurations. The Access Management Console provides enhanced visibility and control of your Access Analyzer findings, and streamlines remediation efforts. Within the console you can track, prioritize, and resolve access issues by assigning tasks.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Access management console, Access Management]
---

# Explore Access management console

Use the Access Management Console within Security Center to review and remediate access issues and misconfigurations. The Access Management Console provides enhanced visibility and control of your Access Analyzer findings, and streamlines remediation efforts. Within the console you can track, prioritize, and resolve access issues by assigning tasks.

Access the console by navigating to **All** &gt; **System Security** &gt; **Security Center** &gt; **Access management console**.

The access management console is divided into 3 tabs:

-   Overview
-   Access findings
-   Access analyzer

## Overview tab

Use the Overview tab to get an overview of access issues and misconfiguration on your instance. From the overview panel you can see your findings and evaluate permissions for users, roles, and groups. You can also review additional resources to learn about user administration on ServiceNow instances.

<table id="table_vv1_ks5_bhc"><tbody><tr><td>

-   **Findings**

Review the findings section, which displays a chart showing access issues and potential misconfiguration detected on your instance. These findings are categorized by severity, with a total count displayed in the center of the chart.

Select the chart, or section of the chart to open the **Access findings** tab, and view a list of access findings.

**Note:** If you had muted a finding, make sure you unmute the finding first to mark the finding as resolved.


</td><td>

![Findings section](../images/acc-1.png)

</td></tr><tr><td>

-   **Access Analyzer**

Use the form in this section to select a user, user group, or role and evaluate its permissions.

Select **Evaluate Access** to evaluate the selected items and see results.

Select the **See all** link to open the **Access analyzer** tab.

For details on using the Access Analyzer diagnostic tool, see [Access Analyzer](../../../integrate/identity/concept/access-analyzer.md), or review the tutorial video and links in the **Access analyzer** tab.


</td><td>

![Access Analyzer section](../images/acc-2.png)

</td></tr><tr><td>

-   **Additional Resources**

Use this section to learn more about access control lists \(ACLs\), user administration, and Security Center.

Select the **Learn More** links to view product documentation about each subject.

Select **Learn more in Security Center** to view the **Security learning and references** page on your instance, which contains links to documentation, user guides, and more for Security Center. To learn more, see [Access Analyzer](../../../integrate/identity/concept/access-analyzer.md) documentation.


</td><td>

![Additional resources section](../images/acc-3.png)

</td></tr></tbody>
</table>## Access findings tab

Use the Findings tab to take a detailed look at your findings, and the checks used to identify them. Findings are potential vulnerabilities that were discovered during the last access check.

<table id="table_u5j_gkd_hhc"><tbody><tr><td>

Access the **Access findings** section by selecting it on the left edge of the screen. This section displays a list of findings.

 Select a finding from the list to open a finding record. From here, you can review information including about the finding and steps to resolve it.

 You can create tasks to resolve a task, mark tasks as resolved, or mute the finding to prevent it from showing in future checks.

</td><td>

![Access findings list](../images/acc-4.png)

</td></tr><tr><td>

Access the **Access checks** section by selecting it on the left edge of the screen.

 This section displays a list of checks that generate your findings, which are run every 24 hours.

 Select a check from the list to review the check record. From here you can review the details of the check, or run immediately using the **Run check** button.

</td><td>

![Access checks list](../images/acc-7.png)

</td></tr></tbody>
</table>## Access analyzer tab

<table id="table_kxr_z4d_hhc"><tbody><tr><td>

Use the access analyzer tab start using the Access Analyzer tool, designed to help administrators view the permissions of an identity for a resource. From this tab, you can use the tool, review previously searched criteria, and review resources to learn how to use Access Analyzer. For more details on this tool and how it's used, see [Access Analyzer](../../../integrate/identity/concept/access-analyzer.md).

</td><td>

![Access analyzer tab](../images/acc-8.png)

</td></tr></tbody>
</table>