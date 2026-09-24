---
title: Goal Framework for SPM release notes
description: The ServiceNow Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow Goal Framework application. See the following sections for release notes by version.Automatic status calculation for targets reduces manual data entry and improves data accuracy by calculating status based on target actual achievement percentages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/goal-framework-for-spm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [goals, targets, status calculation, strategic planning]
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


