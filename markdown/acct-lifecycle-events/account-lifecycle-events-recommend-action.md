---
title: Recommended actions for account onboarding
description: Use Recommended actions to display relevant actions to agents based on a context or condition of a record.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using account onboarding, Account onboarding, Account Lifecycle Events]
---

# Recommended actions for account onboarding

Use Recommended actions to display relevant actions to agents based on a context or condition of a record.

Recommended actions appear as cards in the contextual side panel of your workspace. Depending on the type of record you're working on, these cards contain information to help you find the fastest path to resolution, minimizing the time spent researching and gathering information from different sources.

**Note:**

-   If you are using the Washington DC release, you must installed the Recommended actions for Customer Service \(`sn_cs_nb_action`\) plugin to activate the Recommended Action in the contextual side panel.
-   If you are upgrading from the Vancouver release to Xanadu or Washington DC, if the Recommended Action option is not displayed, you must:
    -   Repair the Recommended Actions - Base Extensions \(`com.snc.next_best_action`\) plugin
    -   Modify the settings in the CSM default record page to activate the page.

        See [KB1650668](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=59d04a084727065048cb2920326d438e) for details.


You can take three types of actions:

-   Guidance: An action that can be performed or helpful information to share.
-   Decision tree: A guided flow to follow that walks you through a series of questions that help you determine the appropriate action.
-   Field recommendations: Recommended values to use for the fields in the record. Recommended field values are auto-filled or shown as messages underneath the fields for the new records. The recommended field values are shown as messages only underneath the fields for the existing records.

The following image shows the recommended actions and troubleshooting tips for the Service Exchange Consumer Registration &amp; Configuration task. To initiate the registration process, click **Start Registration** and follow the guided flow to register the consumer.

![Account onboarding recommended action](../image/account-lifecycle-rec-action.png)

