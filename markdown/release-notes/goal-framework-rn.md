---
title: Goal Framework release notes
description: The ServiceNow Goal Framework application enables your business to create goals, set targets, and evaluate progress toward organizational plans and business outcomes.Track targets that must stay above, below, or within a range of a set value. Customize the prefixes of goal and target numbers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/goal-framework-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [goals, targets, maintain targets, number prefixes]
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Goal Framework release notes

The ServiceNow® Goal Framework application enables your business to create goals, set targets, and evaluate progress toward organizational plans and business outcomes.

## About Goal Framework

-   Create strategic plans, define organizational goals with quantitative or qualitative targets, and establish real-time checkpoints across daily, weekly, monthly, quarterly, and yearly frequencies to track execution.
-   Associate work and planning items—including demand, projects, and portfolios—with strategic goals and targets to provide end-to-end performance visibility across the organization.
-   Support Enterprise PMO \(EPMO\) and portfolio managers with customizable goal preferences, weighted progress calculations, and centralized governance to drive business outcomes aligned to strategic priorities.

See [Goal Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Goal Framework by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 4.16.0

Track targets that must stay above, below, or within a range of a set value. Customize the prefixes of goal and target numbers.

### What's new

-   **[Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-types-gf.md)**

    Track targets that must hold a value for the whole period instead of growing or shrinking toward it. The **Type** field on a target has three new options: **Maintain above**, **Maintain below**, and **Maintain constant**.

    For these types, target progress is the percentage of breakdown periods with actuals where the target was met. For example, if a Maintain above target is met in three of four quarters, its progress is 75%.

    Maintain types are available only with quantitative units of measure. The **Target value distribution** field isn't shown for them.

-   **[Tolerance for Maintain constant targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-maintain-constant-tolerance.md)**

    Set how far a Maintain constant target's actual value can move from the final target and still count as met. By default, an actual value within 5% of the final target, above or below, counts as met. Administrators can change the tolerance with the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

-   **[Unique numbers and prefixes for goals and targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/change-number-prefix-goals-targets.md)**

    Match goal and target numbers to your organization's terminology, for example, OBJ and KR if you use objectives and key results. After an administrator changes the prefix in the number configuration, run the **GF - Override Goal and Target Number fields with customized prefixes** scheduled job to update existing records. The job keeps the numeric part of each number, so GOAL0004512 becomes OBJ0004512. It also skips records that already have the new prefix.


### What's changed

-   **[Target type editable when actuals exist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/change-target-type-gf.md)**

    You can change a target's **Type** after actual values have been recorded. Previously, the **Type** field became read-only once a target had progress. A confirmation message appears before the change is applied, and if you cancel, the **Type** goes back to its original value. Changing the **Type** clears the target's actual value and percent complete. The exceptions are changes between two Maintain types and changes to or from Milestone.

-   **[Type and unit of measure stay in sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/target-types-gf.md)**

    Choosing a target **Type** sets a matching unit of measure:

    -   **Milestone**: Sets the unit of measure to Yes/No, or keeps a custom qualitative unit if one is already selected.
    -   **Maximize**, **Minimize**, or a Maintain type: Restores the last quantitative unit you used, or sets Count \(\#\) if there isn't one.
    The **Type** list always shows all six types. The same pairing also applies to targets created or updated through imports or APIs.


