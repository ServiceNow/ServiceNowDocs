---
title: Configure Success Dashboard indicators KPIs
description: Success Dashboard indicators has a prescriptive methodology for measuring performance. But you can reconfigure the source of the Key Performance Indicators \(KPIs\) by replacing the available indicators in the base system or by adding more indicators.
locale: en-US
release: yokohama
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ITSM Success Dashboard Admin console, Configuring ITSM Success Dashboard indicators, ITSM Success Dashboard indicators, IT Service Management]
---

# Configure Success Dashboard indicators KPIs

Success Dashboard indicators has a prescriptive methodology for measuring performance. But you can reconfigure the source of the Key Performance Indicators \(KPIs\) by replacing the available indicators in the base system or by adding more indicators.

For example, your organization may have a different method to determine **Self-solved using Knowledge**. You cannot change the definition of **Self-solved percentage** and **Call deflection** that use `Self-solved using Knowledge`, but you can replace or add the KPIs and its constituents.

There are two major types of indicators:

-   Primary indicators: The indicators prescribed by ServiceNow.

    **Warning:** You must not modify any primary indicators as these are prescribed by ServiceNow®. Modifying these KPIs might impact your scores.

    -   You can view the primary indicators in the Primary Indicator Registry table `(sn_sd_primary_indicator_registry)`.
    -   You can view the corresponding Performance Analytics indicators in the Primary Indicator table `(sn_sd_primary_indicator)`.

        Primary indicators are of the following types:

        -   Manual: The formulae for these indicators are made up of other primary indicators.
        -   Automatic: The formulae for these indicators are automatically calculated based on the contributing indicators.
-   Contributing Indicators: The indicators listed in the Contributing Indicator Registry `(sn_sd_contributing_indicator_registry)` table and that point to primary indicators.
    -   When these indicators are registered with automatic primary indicators, the formula of the primary indicator is automatically updated to include these indicators in the sum.
    -   When these indicators are removed from the registry or marked inactive, the formula of the primary indicator is updated to remove this indicator from the sum. For example:

        ```
        Self-solve (manual primary indicator) = Self-solved using Virtual Agent (automatic primary indicator) + Self-solved using Knowledge (automatic primary indicator) + Automated Resolutions (automatic primary indicator) 
        ```

        Where:

        -   Self-solved using Virtual Agent = Any Service group issues self-solved using VA \(the only contributing indicator registered for this primary indicator\)
        -   Self-solved using Knowledge = Any Service group issues self-solved using Knowledge \(the only contributing indicator registered for this primary indicator\)
        -   Automated Resolutions \(automatic primary indicator\) = Incident or HR ticket auto-resolution \(the only contributing indicator registered for this primary indicator\)

-   **[Add contributing indicators](add-contributing-indicators.md)**  
Add new contributing indicators based on your organizational preferences.
-   **[Add time savings](add-time-savings.md)**  
Add new time savings as a contributing indicator based on your organizational preferences.
-   **[Update more information cards](update-sidepanel-more.md)**  
Configure and update the **More Information cards** in the side panel.
-   **[Create a cost savings indicator for ITSM Success Dashboard](customize-cost-savings.md)**  
Create a cost savings indicator in ITSM Success Dashboard to determine and display the time saved for the contributing indicators when agents work on an incident.
-   **[Modify the currency code for ITSM Success Dashboard indicators](customize-currency-code.md)**  
Modify the currency code for ITSM Success Dashboard indicators.

**Parent Topic:**[ITSM Success Dashboard Admin console](../concept/admin-console-sd.md)

