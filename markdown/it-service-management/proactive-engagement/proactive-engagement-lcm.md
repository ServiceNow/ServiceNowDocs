---
title: Proactive Engagement life-cycle management
description: The Proactive Engagement application enables you to work in the life-cycle model to manage solutions that you own and to view solutions that may have an impact on services or products that you care about.
locale: en-US
release: yokohama
product: Proactive Engagement
classification: proactive-engagement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Proactive Engagement, Proactive Engagement, Digital End-User Experience, IT Service Management]
---

# Proactive Engagement life-cycle management

The Proactive Engagement application enables you to work in the life-cycle model to manage solutions that you own and to view solutions that may have an impact on services or products that you care about.

You can access the Proactive Engagement workbench by navigating to **All** &gt; **SOW** &gt; **Proactive Engagement workbench**.

The Proactive Engagement Workbench provides an overview of all the Proactive Engagement solutions available on an instance. It displays the details of all the solutions available, deployed, and not deployed.

Deployed solutions, where the engagement settings are configured and are used within the organization. Proactive Engagement resolutions created through the metric rules are deployed by default. For more information, see the [Configuring Proactive Engagement resolutions with DEX](../configuring-metric-rule.md). Deployed solutions can be deployed as custom or original. Solutions created by using the metric rules are original. You can customize the resolution by selecting the deployed record and choosing a custom resolution. Engagement settings for the not deployed solutions are not configured.

## Review solutions for the available updates

For each custom solution where an update is available, the updates can be reviewed by either selecting **Review update** available on the card or when you click on the record to open and access the record. **Review update** provides a comparison between the updated and customized solutions for users to make an informed decision on the next steps. The following actions can be performed:

-   Auto update Removes reference to the custom resolution and will be up to date with the provider solution. The update status is changed to Up to date.
-   Manual update Users go back and manually make any changes required for the solution. The solution update status updates to Manual update pending. Once the changes are done select Solution updated option either on the card or on the Review update page to move the solution update status to Up to date.
-   Ignore update - The update will be ignored, and the solution update status will move to Up to date.

Proactive Engagement will be triggered only for the deployed solutions. There are different **State** in the deployed solutions.

-   **Update available** New updates for out-of-the-box deployed solutions are available.
-   **Update up-to-date** Solution shipped by ServiceNow and is up to date.
-   **Update ignored** Available updates in the provider out-of-the-box solution is ignored.
-   **Pending manual update** Available updates were reviewed and manually updated the solution.

For custom resolutions, you can update them automatically or manually update them. Once the updates are completed, the status changes to Update up-to-date. The **Update provider data** updates or refreshes the solutions in the Proactive Engagement workbench.

**Parent Topic:**[Using Proactive Engagement](../using-proactive-engagement.md)

