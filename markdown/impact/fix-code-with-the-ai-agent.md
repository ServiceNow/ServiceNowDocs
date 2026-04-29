---
title: Bulk Fix code in real-time with Now Assist
description: As a ServiceNow developer, you can receive code fix suggestions when an error is detected.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Fix code in real-time with Now Assist, Now Assist for Platform Health, Platform Health, Using Impact, Impact]
---

# Bulk Fix code in real-time with Now Assist

As a ServiceNow developer, you can receive code fix suggestions when an error is detected.

## Before you begin

Complete the pre-requisites and setup steps in order to activate Fix code in real-time. See [Configure Fix code in real-time for Platform Health](../concept/configure-ai-code-fix-for-platform-health.md) for details.

Role required: sn\_impact\_gen\_ai\_fix\_user

## Procedure

1.  If an error is detected that is eligible for an AI resolution, the **Fix with Now Assist** button will become visible.

    A findings message displays with the following information:

    -   **Finding level state**: Act, Recommend, Suggest, or Review.
        -   The ServiceNow leading practice issue finding and explanation is included.
        -   Select the link to view the Scan Engine definition.
        -   Findings for that definition are listed in the related lists for the definition record.
    -   **Details**: Exact location in the code of the finding
    -   **Steps to resolve issue**: Description of resolution
    -   **Supporting documentation**: A link to KB or documentation explaining the recommended configuration
    -   **Impact**: A rating on a scale of 1:10 on how the error can impact the overall code basis, with 10 having the most impact. Details are in the Scan Engine definitions details.
    ![Example Scan Engine code fix finding.](../image/code-fix-ai-finding-message.png)

2.  Select **Fix with Now Assist** from the menu bar to execute the remediation process.

    Review the Now Assist Panel with remediation suggestions.

    ![The suggested fix for the Code Fix AI finding.](../image/code-fix-ai-remediation.png)

    -   The Now Assist panel displays the reasoning, in steps, for the findings it provided resolutions for.
    -   At the same time, a code comparison view displays on the script itself, illustrating the suggested modifications. Updated code is displayed in green and the removed code has a pink background.
    -   The script editor is read-only until the Now Assist conversation closes, either by accepting or rejecting the proposed fix.

        **Note:** You can either accept the code fix as is, reject it, or provide revisions to the suggested fix. During the revision process, you can interact with the AI Agent panel to prompt it to make additional changes for each finding.

3.  Enter **Accept the solution** in the AI response prompt to make the change.

    -   The available prompts are displayed in the bulleted list for the proposed solution.
    -   If you reject the solution, the code will be editable.
    **Note:** Users with the executive role can access the Executive Dashboard which contains a module that displays all findings resolved using the Code Fix AI Agent. See [Scan Engine Executive dashboard](../concept/scan-engine-executive-dashboard.md) for additional information.


