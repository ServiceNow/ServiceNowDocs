---
title: Setup Telecommunications Customer 360
description: Use the Telecom Customer 360 guided setup to configure the unified customer view for your organization. Complete the three setup tasks to define your cards and configure their data and settings. Verify the page layout before customer service agents use it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/telecom-cust-360-landing.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Setup Telecommunications Customer 360

Use the Telecom Customer 360 guided setup to configure the unified customer view for your organization. Complete the three setup tasks to define your cards and configure their data and settings. Verify the page layout before customer service agents use it.

## Before you begin

Role required: `sn_telecom_c360.admin`

## About this task

Use the guided setup option to review the default configuration for the Telecommunications Customer 360 view, and make changes if required. You can skip individual tasks if no changes are needed, but all three tasks must be marked complete before the setup is finished.

## Procedure

1.  Navigate to **All** &gt; **Telecom Customer 360** &gt; **Guided Setup** and select **Get Started**.

    \[Omitted image "guided-setup.jpg"\] Alt text: Telecom Customer 360 guided setup

2.  Complete the **Define 360 cards** task.

3.  Select the **360 Cards** tab.

    The following cards are included with the base system:

    -   Insights
    -   Contact card
    -   Interaction history
    -   Data visualization group
    -   Billing
    -   Products
    -   All tasks
4.  To update an existing card definition, select **Configure**, select the card you want to edit, follow the steps on the guided setup page and select **Mark as Complete**.

5.  Select the **360 Variables** tab.

    Card variables define the configurable properties for each card, such as data tables, query conditions, and display fields. Review or update the variables associated with each card and select **Mark as Complete** to unlock the next task.

6.  To create a custom card, select **Configure** and then select **New** and fill in the required fields.

    Creating a custom card only defines the card's metadata. To display the card in the Telecom Customer 360 view, you must also add it to the page in UI Builder. See [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md) for details.

7.  Complete the **Configure 360 card data and settings** task.

    Use this task to configure the data, display, and visibility settings for each card for the three supported contexts: account, consumer, and contact. Select **Configure** and review or update the following:

    -   Context table, card variables, and query conditions that determine the data to be retrieved.
    -   Fields and columns to be displayed on the card.
    -   User roles to restrict access to specific users.
    **Note:**

    -   To override or change the default card setting, clone the card setting, modify it as required, and set a higher order than the default setting.
    -   To create a role specific experience, create card setting record, define the context table and variables, and set a specific role and higher order than the default setting.
8.  Complete the **Configure 360 view** task.

9.  Select **Configure** to open the Telecom Customer 360 record page variant in UI Builder.

    **Note:** The Telecom Customer 360 record variant is set to Read-only. Do not edit the Telecom Customer 360 record variant directly to preserve the base configuration and avoid upgrade conflicts. Clone the record variant, set an appropriate order, update the variant condition and audience on the new version. See [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md) for details.

10. Select **Mark as Complete**.


## Result

After the cards have been configured, customer service agents can start using the Telecommunications Customer 360 application. See [Telecommunications Customer 360 home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-home-page.md) for details.

-   **[Configure the Telecommunications Customer 360 variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-configure-variables.md)**  
Configure the properties for each card, such as data tables, query conditions, and display fields.

**Parent Topic:**[Configure Telecommunications Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-configure.md)

