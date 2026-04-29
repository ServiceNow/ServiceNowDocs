---
title: Report an issue using Now Assist for Manufacturing Commercial Operations \(MCO\)
description: Use the MCO portal to submit product non-conformance issues with AI-guided playbook workflows for duplicate detection, completeness assessment, cost tracking, and review. This improves data consistency, traceability, and efficiency.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for MCO, Manufacturing Commercial Operations]
---

# Report an issue using Now Assist for Manufacturing Commercial Operations \(MCO\)

Use the MCO portal to submit product non-conformance issues with AI-guided playbook workflows for duplicate detection, completeness assessment, cost tracking, and review. This improves data consistency, traceability, and efficiency.

## Before you begin

Role required: Product Non-conformance Submitter

## About this task

The Enhance non conformance description AI skill evaluates the non-conformance descriptions and suggests improvements to verify clarity and completeness.

## Procedure

1.  Navigate to **Dealer Portal** &gt; **Report an issue**.

2.  In the Create New Product Non-conformance Case, select **Quick start** activity.

    1.  Select **Install Base** from the list.

    2.  Select **Continue**.

        The Account/Service organization/Consumer name is retrieved for the selected install base item.

    3.  Select **Continue**.

3.  In the **Describe the issue** field, enter the issue description in your own words.

    The description is evaluated for 5W2H that is what where, when, who, why, and how. Based on the information provided.

    1.  Select **Suggestions for improvement** to get assistance from Now Assist ![](../../../common/image/icon-ai-sparkle.png).

    2.  Select + to add the supporting document and work orders.

    3.  Select **Save**.

    4.  Select **Continue**.

4.  Proceed without entering the detials in the **Follow-up** activity.

    -   Now Assist ![](../../../common/image/icon-ai-sparkle.png) analyzes the issue description and attachments to auto-populate answers to the follow-up questions.
    -   You can edit the auto-populated answers by selecting the form fields and **Continue**.
5.  In the **Identify duplicate**, check if there's any existing NCC for the same install base item.

    The system searches the existing NCCs in the same install base, compares short description and description, and returns the top match based on confidence score. Confidence score is the matching percentage between the existing NCC and the new submission.

    -   Yes, this is a duplicate: The report exits the flow and this draft is closed as a duplicate. You’re redirected to the existing parent NCC.
    -   No, continue with the new NCR: The draft report continues.
6.  In the **Add correction action** activity, update whether the correction action is already applied to resolve the issue.

    -   No: It enables you to continue to **Review and Submit**. You can select this option anytime before selecting **Continue**. It deletes the new correction details that you added.
    -   Yes: **Add correction details** and **Expense line** are enabled.

        |Field|Description|
        |-----|-----------|
        |Add Correction details|
        |Short description|Short description of the correction action taken to resolve the issue.|
        |Description|Detailed description of the correction action taken to resolve the issue.|
        |Expense line|
        |Description|Short description of the expense line.|
        |CoPQ type|Cost of poor quality type.|
        |Asset|Type of asset.|
        |Amount|Cost of the labor or administrative, or cost incurred to procure a new item.|

    Add multiple correction actions by selecting **Add**.

7.  Select **Continue** to save your changes.

8.  In the Review and submit section, review all the 5W2H details, correction actions, and the expense lines tagged to the correction actions.

    Review and edit any values. Add additional information if needed, then select **Submit**.

    The submitted issue reference number is generated.


