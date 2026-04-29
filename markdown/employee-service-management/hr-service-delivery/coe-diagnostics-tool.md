---
title: Use COE Security Diagnostics
description: Enable HR administrators to determine how the COE \(HR Centers of Excellence\) security policies are evaluated for HR agents.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR service categorization, HR Centers of Excellence data model, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Use COE Security Diagnostics

Enable HR administrators to determine how the COE \(HR Centers of Excellence\) security policies are evaluated for HR agents.

## Before you begin

Role required: sn\_hr\_core.admin

**Note:** COE security diagnostics:

-   should not be used to find the overall access of a case for a given HR agent. It should only be used for analyzing how COE security policies are evaluated.
-   does not cover all access scenarios and may differ from actual access results. For example, Opened for, Opened by, Watch List, and Collaborators get access to an HR case irrespective of its security policies. Use [Access Analyzer](https://www.servicenow.com/docs/access?context=access-analyzer&version=australia&pubname=australia-platform-security&ft:locale=en-US) for complete access analysis and accurate results.
-   For Frequently Asked Questions \(FAQs\), see [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2757698).

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Security Diagnostics**.

<table id="table_jyp_n3v_13c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HR case

</td><td>

Option to select an HR case for which you want to analyze the COE security policies.**Note:** The HR admin who is using COE Security Diagnostics must have access to HR cases that are being evaluated.

</td></tr><tr><td>

User

</td><td>

Option to select the HR agent for whom you want to analyze the COE security policies.

</td></tr><tr><td>

Operation

</td><td>

Option to check the type of access the HR agent has on the given HR case. -   Read
-   Write


</td></tr></tbody>
</table>2.  Select **Diagnose** to view the evaluation results.

    -   Can read/Cannot read/Can Write/Cannot write: Message indicating the reason why the HR agent does or does not have to access to the HR case.
    -   COE Security Policies: List of evaluated policies.

        -   Policies are evaluated only if case COE matches the policy COE or case COE is a child of policy COE and **Applies to all child COEs** is enabled on that policy.
        -   Write policies are evaluated for read access.
        -   Evaluation stops once the matching policy passed the requirements.
<table id="table_tdm_mlv_13c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Displays the policy name.

</td></tr><tr><td>

HR Service match

</td><td>

Indicates whether the case is matching the HR service configured in the COE security policy.**Note:** If **Applied to all services** is checked on the policy, the policy matches all HR cases of the COE.

</td></tr><tr><td>

Condition match

</td><td>

Indicates whether the condition defined in the COE security policy matches with the HR case.**Note:** If condition is set to empty on this policy, then it matches all the HR cases.

</td></tr><tr><td>

Group match

</td><td>

Indicates whether the HR agent matches any of the groups.

</td></tr><tr><td>

Matched group

</td><td>

Indicates the name of first group matched for the HR agent.

</td></tr><tr><td>

Result

</td><td>

-   **Skipped**: Indicates that the HR case does not match either HR service or Condition.
-   **Failed**: Indicates that the HR case matches both HR service and Condition of the policy, but user is not member of any user group.
-   **Passed**: Indicates that the HR case matches HR service, and condition, and user matches one of the groups.


</td></tr></tbody>
</table>
**Parent Topic:**[HR service categorization](hr-service-categorization.md)

