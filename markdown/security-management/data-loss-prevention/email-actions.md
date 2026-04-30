---
title: Email remediation actions
description: Perform the remediation action on the email quarantined for Proofpoint.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-09-19"
reading_time_minutes: 1
breadcrumb: [Create a Profile for Proofpoint DLP integration, Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Email remediation actions

Perform the remediation action on the email quarantined for Proofpoint.

## Before you begin

Proofpoint provides four remediation actions:

1.  Release Email with Scan
2.  Release Email without Scan
3.  Release Encrypted Email with Scan
4.  Delete Email

By default, **Release Email with Scan**, **Release Email without Scan, Release Encrypted Email with Scan**, and **Delete Email response options** and **Proofpoint Remediation Action Rule** to perform the remediation action on the email. These response options also have the **Proofpoint Email Release Approval Rule** configured with it to leverage the approval functionality for these actions. These remediation actions are available to the End Users, Analysts, Escalated Incident Reviewers for execution.

For more information, see [Set up incident response option rules for your DLP incidents](https://servicenow.com/docs/bundle/xanadu-security-management/page/product/data-loss-prevention/task/configure-end-user-action.html), [Configure response option for your DLP incidents](https://servicenow.com/docs/bundle/xanadu-security-management/page/product/data-loss-prevention/task/configure-response-option-mapping.html), and [Configure Approval Rules](https://servicenow.com/docs/bundle/xanadu-security-management/page/product/data-loss-prevention/task/configure-approval-rules.html).

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst

![Proofpoint Quarantine Release Response Option Rule](../image/dlp-proofpoint-release-response-option-rule.png "Proofpoint Quarantine Release Response Option Rule")

![Proofpoint Quarantine Release Response Option Mappings](../image/dlp-proofpoint-release-response-option-mapping.png "Proofpoint Quarantine Release Response Option Mappings")

## Procedure

1.  The following procedure explains how to submit the remediation action from the DLP Analyst Workspace. As a DLP Admin and DLP Analyst, you can:
2.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

3.  Open any Proofpoint DLP incident with **Scan source** as Email SMTP.

4.  Click **Respond**.

5.  Select the response option from the **Response** drop down list.

6.  Click **Submit**.

7.  The following procedure explains how to submit the remediation action from the DLP User Workspace. As an end user, you can:
8.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

9.  Open any Proofpoint DLP incident with **Scan source** as Email SMTP.

10. Click **Respond**.

11. Select the response option from the **Response** drop down list.

12. Click **Submit**.

    **Note:**

    -   When an approval rule is configured for this action, the approval flow will be triggered first and after receiving all the approvals, the email remediation flow will be triggered, and then the action will be performed.
    -   If **Delete Email** is performed, then the state of the DLP incident is updated to **Delete File**. For any other response option, the DLP incident state will be updated to **Released Email from Quarantine** after the email is successfully released.

**Parent Topic:**[Create a Profile for Proofpoint DLP integration](create-profile-proofpoint-dlp-integration.md)

