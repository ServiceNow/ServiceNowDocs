---
title: Submit the assessment
description: Log in as an assessor of the Importance and impact tolerance assessment, respond to the questionnaire, and submit the assessment in Operational Resilience Workspace for an approval.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Performing Importance and impact tolerance assessment, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Submit the assessment

Log in as an assessor of the Importance and impact tolerance assessment, respond to the questionnaire, and submit the assessment in Operational Resilience Workspace for an approval.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **List** &gt; **Importance and impact tolerance assessment** &gt; **All assessments** and open the assessment that you’re working on.

2.  Log in as the assessor of the assessment.

3.  Add operational vulnerabilities relevant to the service from the **Operational vulnerabilities** tab.

4.  On the **Assessment** tab, select the assessment and respond to the questions.

    As an assessor, you can respond to the questions.

    The assessment is created and visible in the **Assessment** tab, accessible only to the assessment owner and assessor. When the assessment owner attempts to access the assessment, a message indicates that it is assigned to another user. The owner can view it in read-only mode or edit it, which reassigns write access from the assessor to the owner.

5.  To add a contributor to the assessment, select the Contributors icon ![Contributor icon.](../../../reuse/icons/product-icons/user-group-outline-24.svg) on the contextual sidebar.

    The Contributors icon is displayed with the installation of the Smart Assessment Collaboration \(sn\_smart\_collab\) plugin.

    1.  Select the **+ Add** button.

    2.  On the **Add contributors** pop-up, add the names of the users in **Select users to add to this assessment** field.

        **Note:** By default, the Operational Resilience application filters users and displays only those with the sn\_oper\_res.user role or higher. The assessment owner can then select from these available users to add to the assessment.

    3.  Select **Add contributors**.

        Contributors can view the assessment from the list view or from the Tasks page. They can respond to the assessment and save their changes, but they cannot submit it. Only primary owners of the assessment can submit them.

6.  To finish a pending assessment, select **All questions** or **Unanswered questions**.

    You can either view all questions or filter to see only the unanswered questions.

7.  Respond to the questions, verify that you have answered all the questions, and save your responses.

8.  To reassign the assessment, select **Reassign** from the **More options** menu.

    A confirmation message appears, warning that reassigning the assessment results in losing your current access to it. You can confirm and proceed to the next step. If the reassignment is done, the user has access to the Importance assessment.

    1.  Select the desired user from the list in the modal and select **Reassign**.

    The assessment is reassigned to the selected user from the list.

9.  To submit the assessment, select **Submit**.

    A confirmation message appears, stating that you have reviewed your answers and understand that submission is final and may prevent further changes.

10. Select the check box to confirm that you have reviewed the answers and select **Submit** again.

    A confirmation message is displayed, indicating that the update has been successfully processed and the assessment has been submitted.

11. Refresh the **Assessment** tab to confirm that the Importance assessment is complete and its status is Completed.

    After the assessment is submitted, its state changes to **Assessment received**. This triggers an automation flow, resulting in an update to the IIA value on the IIA page.

    The Importance and impact tolerance assessment now includes three additional fields: **Customer impact**, **Financial impact**, and **Transactional volume**, which are used to determine the overall impact tolerance values based on assessment results.

    **Note:**

    After the assessment is completed and it is in the **Assessment received** state, the owner has the option to override the calculated impact tolerance values if necessary.

    Once the assessment is completed and it is in the **Assessment received** state, the owner can override the calculated impact tolerance values if needed. Upon completion of all assessments, the IIA automatically transitions to the **Assessment received** state, and the importance values are updated in the **Scope** tab.

    **Note:** Unlike Legacy assessments, where retaking an assessment was not possible, the Smart Assessment method allows you to reopen and retake assessments. If an assessment is canceled or rejected, it reverts to the **Pending response** state, enabling users to retake it, unlike the Legacy system where it remained in the **Assessment received** state.

    Only the assessment's requester/owner and assigned assessor can reopen a completed assessment; contributors assigned to the assessment do not have this capability.

    Email notifications are sent at various stages, including IIA creation, scope updates, assessment assignments, reassessments, and when collaborators are added, to keep stakeholders informed throughout the process.


## What to do next

The owner of the Importance and impact tolerance assessment \(IIA\) requests for an approval. For more information, see [Request an approval for the assessment](verify-response-to-the-assessment-in-ws.md). If no approvers are specified, the record moves to the **Approved** state.

