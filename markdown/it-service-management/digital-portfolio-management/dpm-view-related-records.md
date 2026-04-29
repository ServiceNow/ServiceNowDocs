---
title: View relationships of business applications and service instances in the DPM Admin Center
description: In the DPM Admin Center, you can see a comprehensive view of your business applications and service instances. You can see incidents, problems, and changes that are related to your business applications and incidents and changes that are related to your service instances.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure the Admin Center, Configure, Digital Portfolio Management, IT Service Management]
---

# View relationships of business applications and service instances in the DPM Admin Center

In the DPM Admin Center, you can see a comprehensive view of your business applications and service instances. You can see incidents, problems, and changes that are related to your business applications and incidents and changes that are related to your service instances.

The relationships of business applications and service instances enable you to see a full picture of your solutions. For example, business applications consume multiple service instances. So if you set a configuration item \(CI\) for an incident, you must select the service instance that the incident belongs to. After that CI is set up, the incident rolls up to the business application that consumes that service instance. You can see all the relationships from the DPM Admin Center.

**Important:** To access the DPM Admin Center, you must have the DPM admin \[sn\_dpm.dpm\_admin\] role.

## View business applications related to changes for build metrics

-   Access the **Overview** tab in the DPM Admin Center, and then select **Configure** in the Business applications card.
-   Select **4 Assess build metrics** in the navigation bar.
-   View the **Business applications related to changes** card.
-   Select a numbered item on the card to see the business applications related to changes through the following criteria.

    -   The business application field
    -   The configuration item field
    -   The affected CIs
    -   The impacted services
    **Note:** A card is set to **Ready for DPM** when any one of the listed criteria is greater than zero. If you select zero \(0\) on a card, then an empty state displays.

    After you select a numbered item on the card, another tab opens with a grouped list of each business application that's related to changes according to the criterion that you selected. You can open a business application on the list and drill down to each record number to see the related items details \(consumes, depends on, and so on\).


## View business applications related to incidents, problems, and changes for operational metrics

-   Access the **Overview** tab in the DPM Admin Center, and then select **Configure** in the Business applications card.
-   Select **5 Map KPI groups** in the navigation bar.
-   View the cards under the **Map KPI groups** heading. Each card shows the following with numbered items.
    -   Business applications related to incidents
    -   Business applications related to problems
    -   Business applications related to changes
-   Select a numbered item in any of the cards to see the business applications related to incidents, problems, or changes through the following criteria.

    -   The configuration item field
    -   The affected CIs
    -   The impacted services
    **Note:** A card is set to **Ready for DPM** when any one of the listed criteria is greater than zero. If you select zero \(0\) on a card, then an empty state displays.

    After you select a numbered item on the card, another tab opens and displays a grouped list of each business application that's related to that criterion. You can open a business application on the list and drill down to each record number to see the related items details \(consumes, depends on, and so on\).


## View applications services related to incidents and changes for operational metrics

-   Access the **Overview** tab in the DPM Admin Center, and then select **Configure** in the Service instances card.
-   Select **3 Map KPI groups** in the navigation bar.
-   View the cards under the **Map KPI groups** heading. Each card shows the following with numbered items.
    -   Service instances related to incidents
    -   Service instances related to changes
-   Select a numbered item in either of the cards to see the business applications related to incidents or changes through the following criteria.

    -   The configuration item field
    -   The affected CIs
    -   The impacted services
    **Note:** A card is set to **Ready for DPM** when any one of the listed criteria is greater than zero. If you select zero \(0\) on a card, then an empty state displays.

    After you select a numbered item on the card, another tab opens and displays all the service instances related to your selected criterion. For example, you could see all service instances related to incidents through affected CIs. In this example, you can drill down to see the source incident record.


**Parent Topic:**[Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md)

**Related topics**  


[Use the Admin Center in Digital Portfolio Management](dpm-admin-center.md)

