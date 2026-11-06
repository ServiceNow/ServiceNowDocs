---
title: Generate and modify resolution steps in LEAP
description: Learn how to generate, edit, and track AI-generated resolution steps for automation opportunities in LEAP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generating-and-modifying-resolution-steps.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 3
breadcrumb: [Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Generate and modify resolution steps in LEAP

Learn how to generate, edit, and track AI-generated resolution steps for automation opportunities in LEAP.

## About this task

Resolution steps are actions that resolve issues identified by an automation opportunity. During the initial run, GAF generates these steps by analyzing work notes and historical resolutions.

Resolution steps are generated from the work notes, comments, and other details in the record. The more complete and accurate your records are, the more useful the generated resolution steps are.

The **Generate resolution steps** button creates resolution steps as required. As your system processes new incidents and records, regenerate these steps to maintain solution accuracy. LEAP provides three search capabilities: AI search, KB search, and web search.

-   AI search: Scans records within your existing instance to identify relevant resolutions.
-   KB search: Searches knowledge base resources external to your organization to suggest more effective resolution steps.
-   Web search: Queries web resources beyond your organization's systems to find comprehensive solutions, broadening the scope of potential resolutions.

Before LEAP generates or regenerates resolution steps, the **Select sources** dialog box lets you choose the sources that enhance the steps:

-   **KB articles**: Enhances the resolution steps with details from KB articles in this instance that match the problem.
-   **Web search**: Enhances the resolution steps with details from a web search. Only the problem summary is sent, not your records.

Both sources are selected by default. Clear a source to exclude it. To keep your selection for future generations in the project, select **Remember my choices for this project**. You can also change these choices on the LEAP settings page. For details, see [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

**Note:**

-   Regenerating resolution steps incurs chargeable transactions. Exercise caution and careful planning before using the regenerate button to avoid unexpected costs.
-   Only a system administrator or a LEAP admin with system administrator access can enable these additional sources of searches. Users with agent or viewer access must contact their administrator to activate these features. Once enabled, LEAP expands its search capabilities to deliver more comprehensive and effective resolution steps.
-   In the **Select sources** dialog box, a source that is not available appears disabled and you can't select it. If AI Search isn't enabled, the dialog box displays "KB search is not available. Ask your administrator to enable AI Search." If the Web Search plugin isn't enabled, it displays "Web search is not available. Ask your administrator to enable the Web Search plugin."

Resolution steps are generated only for automation opportunities that match the **Default resolution steps filter** configured in LEAP settings. The default filter is set to Critical priority \(`automation_priority=40`\). Items are processed in batches in the background, so performance is not affected during generation. To change the priority filter, update the condition builder in [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

## Before you begin

Role required: LEAP admin

## Procedure

1.  Select **Workspaces** &gt; **LEAP**.

2.  On the LEAP landing page, select the required automation opportunity.

3.  If resolution steps are unavailable in the Overview section, select **Generate resolution steps**.

4.  In the **Select sources to generate resolution steps** dialog box, select the sources to use, and then confirm to start generation.

    To keep your selection for future generations in the project, select **Remember my choices for this project**.

5.  If resolution steps are available, and you want to get alternative resolution steps, then use the **Regenerate** button.\[Omitted image "regenerate-resolution-steps-gradient.png"\] Alt text: Regenerate resolution steps

    **Note:**

    -   The Regenerate button is turned off while manual editing is in progress.
    -   Resolution steps are generated using the sources you select in the **Select sources** dialog box.
6.  In the **Select sources to enhance resolution steps** dialog box, select or clear the sources to use, and then select **Regenerate**.

    To keep your selection for future generations in the project, select **Remember my choices for this project**.

7.  To manually modify resolution steps, select the edit icon.

    Each update to the resolution steps is recorded in the LEAP Outcome Snapshots table for traceability.

8.  To revert to the last generated resolution steps, use the **Revert to AI generated steps** button.


## Result

