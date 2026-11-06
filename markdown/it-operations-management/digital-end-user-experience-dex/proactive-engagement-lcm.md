---
title: Proactive Engagement life-cycle management
description: The Proactive Engagement application supports life-cycle management of solutions. Use it to manage solutions you own and to view solutions that affect your services or products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/proactive-engagement-lcm.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use Proactive Engagement, Digital End-User Experience, IT Operations Management]
---

# Proactive Engagement life-cycle management

The Proactive Engagement application supports life-cycle management of solutions. Use it to manage solutions you own and to view solutions that affect your services or products.

You can access the Proactive Engagement workbench by navigating to **All** &gt; **Service Operations Workspace** &gt; **DEX Administration** &gt; **Proactive Engagement workbench**.

The Proactive Engagement Workbench provides an overview of all the Proactive Engagement solutions available on an instance. It displays the details of all the solutions available, deployed, and not deployed.

Deployed solutions are solutions whose engagement settings are configured and that are used within the organization. Proactive Engagement resolutions created through the metric rules are deployed by default. For more information, see [Configure Proactive Engagement resolutions with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configuring-metric-rule.md). Deployed solutions can be deployed as custom or original. Solutions created by using the metric rules are original. You can customize the resolution by selecting the deployed record and choosing a custom resolution. Engagement settings for the not deployed solutions are not configured.

## Available solution updates

For each custom solution where an update is available, you can review the updates by selecting **Review update** on the card or by opening the record. **Review update** provides a comparison between the updated and customized solutions for users to make an informed decision on the next steps. The following actions can be performed:

-   **Auto update**: Removes the reference to the custom resolution and keeps the solution up to date with the provider solution. The update status changes to Up to date.
-   **Manual update**: Users manually make any changes required for the solution. The solution update status changes to Manual update pending. After the changes are done, select the **Solution updated** option either on the card or on the Review update page to move the solution update status to Up to date.
-   **Ignore update**: The update is ignored, and the solution update status moves to Up to date.

Proactive Engagement is triggered only for the deployed solutions. Deployed solutions can be in the following states.

-   **Update available**: New updates for base system deployed solutions are available.
-   **Update up-to-date**: The solution shipped by ServiceNow is up to date.
-   **Update ignored**: Available updates in the provider base system solution are ignored.
-   **Pending manual update**: Available updates were reviewed, and the solution must be updated manually.

For custom resolutions, you can update them automatically or manually update them. After the updates are completed, the status changes to Update up-to-date. The **Update provider data** option refreshes the solutions in the Proactive Engagement workbench.

**Parent Topic:**[Using Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/using-proactive-engagement.md)

