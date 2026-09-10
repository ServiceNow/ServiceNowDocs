---
title: Goal Framework for SPM release notes
description: The ServiceNow Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow Goal Framework application. Goal Framework for SPM was enhanced and updated in the Zurich release.The ServiceNow Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow Goal Framework application. Goal Framework for SPM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Goal Framework for SPM release notes

The ServiceNow® Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow® Goal Framework application. Goal Framework for SPM was enhanced and updated in the Zurich release.

## About Goal Framework for SPM

Use the sn\_gf\_goal\_admin role to update the goal-specific system properties.

See [Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/goal-framework.md) for more information.

## Activation and other requirements

**Important:** Goal Framework for SPM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-business-management-rn-landing.md)

## Zurich

The ServiceNow® Goal Framework for SPM application enables you to automate the actual value of your targets for the goals that are defined using the ServiceNow® Goal Framework application. Goal Framework for SPM was enhanced and updated in the Zurich release.

### What's changed

-   **[Goal system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/components-installed-with-goal-framework.md#section_myd_rzy_fyb)**

    Users with the sn\_gf\_goal\_admin role assigned can update goal-specific system properties:

    -   **sn\_gfa.weeklyCheckInDayToMapMonth** - Defines the end day of the week used for mapping weekly target breakdowns to a month. The default value is Friday.
    -   **glide.ui.sn\_gf\_goal\_target\_activity.field** - Enables activity stream for fields of the targets.
    -   **sn\_gfa.target\_breakdown\_decimals** - Sets the number of decimal places displayed for target values when generating target breakdowns. The default value is 2.

