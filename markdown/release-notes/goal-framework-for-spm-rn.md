---
title: Goal Framework for SPM release notes
description: The ServiceNow Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow Goal Framework application. See the following sections for release notes by version.Track targets that must stay above, below, or within a range of a value, and measure their progress by how many check-in periods meet the target.Automatic status calculation for targets reduces manual data entry and improves data accuracy by calculating status based on target actual achievement percentages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/goal-framework-for-spm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [goals, targets, maintain type, target breakdowns, progress calculation, goals, targets, status calculation, strategic planning]
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Goal Framework for SPM release notes

The ServiceNow® Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow® Goal Framework application. See the following sections for release notes by version.

## About Goal Framework for SPM

-   Align work items to goals and targets, and automate actual value updates by configuring target sources, ensuring real-time progress tracking without manual updates.
-   Set target breakdowns at daily, weekly, monthly, quarterly, or yearly intervals. Distribute the final target value cumulatively or non-cumulatively across the defined time duration.

See [Goal Framework and Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 2.12.0

Track targets that must stay above, below, or within a range of a value, and measure their progress by how many check-in periods meet the target.

### What's new

-   **[Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-types-overview.md)**

    Track targets that need to hold steady at a value over time, such as keeping server uptime above 98% for a year. In addition to **Maximize** and **Minimize**, the **Type** field on a target includes three options:

    -   **Maintain above**: The actual value must stay at or above the final target.
    -   **Maintain below**: The actual value must stay at or below the final target.
    -   **Maintain constant**: The actual value must stay within a tolerance range of the final target.
    When you select a Maintain type, the **Target distribution** field is hidden on the target form.

-   **[Progress calculation for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-types-overview.md#section_maintain_targets)**

    Measure progress on Maintain-type targets by how consistently the metric meets the target across check-in periods. The system automatically calculates status for each target breakdown period that has an actual value:

    -   **Maintain above**: Green when the actual is at or above the final target, and Red when it's below.
    -   **Maintain below**: Met when the actual is at or below the final target.
    -   **Maintain constant**: Met when the actual falls within the tolerance range, bounds included.
    Target-level progress equals the number of periods that meet the target divided by the total periods up to the latest actual value, multiplied by 100. For example, a **Maintain above** target with a final target of 75 and quarterly actuals of 78, 72, 80, and 76 shows 75% progress. Three of 4 periods meet the target.

-   **[Target breakdowns for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-breakdowns.md#section-maintain-type-breakdowns)**

    Start every check-in period from the same value. When you save a Maintain-type target, each target breakdown gets a planned target equal to the final target value. You can edit the planned target of any breakdown. If the final target value is empty, breakdowns are created with a planned target of 0.


### What's changed

-   **[Target breakdown regeneration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-breakdowns.md#section-maintain-type-breakdowns)**

    Target breakdowns adjust to changes in a target's dates or final target value, and recorded actuals are kept:

    -   Moving the start date later removes the breakdowns before the new start date. The remaining breakdowns keep their planned targets and actuals.
    -   Moving the start date earlier adds breakdowns for the new periods, with the same planned target.
    -   Shortening or extending the end date removes or adds the matching breakdowns.
    -   Changing the final target value updates the planned target of every breakdown and recalculates status and progress.
-   **[Type field editable after actuals are recorded](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/change-target-type-spw.md)**

    Change the **Type** of a target after actual values are recorded, without deleting and recreating the target. When you change the type from Maximize to Minimize, or from Maximize to a Maintain type:

    -   The total actuals to date stay the same and are placed in the latest target breakdown period.
    -   Planned values are recalculated for the new type.
    -   Progress and attainment are recalculated using the new type's logic.
    A warning appears before you save the change. The change is recorded in the audit history.

-   **[Number field in the target list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-form-egm.md)**

    The **Number** field appears as a link in the actual value automation list view. That list view opens when you view targets in Core UI.


## Version 2.10.0

Automatic status calculation for targets reduces manual data entry and improves data accuracy by calculating status based on target actual achievement percentages.

### What's new

-   **[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/automatic-status-calculation-targets.md)**

    Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

    Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-automatic-status-calculation.md)**

    Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

    Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.


### What's changed

-   **Default check-in frequency**

    New quantitative targets now default to **Quarterly** check-in frequency to create target breakdowns when you save the target. You can change the check-in frequency before creating the target.

-   **Improved status labeling**

    The **None** status option is now labeled **No status** for goals, strategic priorities, target progress, and target breakdowns, providing clearer communication about goal status states.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


