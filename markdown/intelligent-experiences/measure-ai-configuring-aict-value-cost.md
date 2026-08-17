---
title: Configuring Cost in AI Control Tower
description: Use the cost setup wizard to set the hourly rate and AI usage costs, so that AI Control Tower can express value in money and calculate net returns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/measure-ai-configuring-aict-value-cost.html
release: zurich
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Configuring Cost in AI Control Tower

Use the cost setup wizard to set the hourly rate and AI usage costs, so that AI Control Tower can express value in money and calculate net returns.

## Cost overview

The Cost setup page displays a value and cost configuration summary based on the hourly rates and vendor costs you have configured. The system calculates three key metrics over a configurable time period:

-   **Total savings**: Productivity gains measured in hours, multiplied by the average hourly rate configured in your system.
-   **Total Enterprise AI cost**: The sum of integrated vendor costs and other vendor costs associated with your AI assets.
-   **Net returns**: The financial return calculated as total savings minus total enterprise AI cost.

## Configuration components

Cost setup includes the following configurable elements:

-   **Avg hourly rate**

    The average hourly rate used to calculate productivity savings. This rate is multiplied by the total hours saved to determine financial benefit.

-   **Integrated vendor costs**

    The costs associated with integrated AI vendors included in your AI asset portfolio.

-   **Other vendor costs**

    Additional vendor costs not classified as integrated vendor costs.


## Configuring cost setup

To modify cost configuration settings, select **Edit configuration** on the Cost setup page. This allows you to adjust hourly rates, vendor costs, and other parameters that impact your cost calculations.

**Note:** The Cost setup page displays data refreshed as of the last configuration update. Select **Refresh** to retrieve the latest calculated values based on your current configuration.

