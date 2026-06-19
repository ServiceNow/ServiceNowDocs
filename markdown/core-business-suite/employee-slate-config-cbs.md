---
title: Employee Slate configuration for CBS
description: Core Business Suite provides two setup options for configuring Employee Slate as the default employee support portal. You can select any one according to your organizational requirement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/employee-slate-config-cbs.html
release: australia
product: Core Business Suite
classification: core-business-suite
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 1
keywords: [Employee Slate, Employee Experience, Core Business Suite, Moveworks, Now Assist, employee portal, configure]
breadcrumb: [Configure, Core Business Suite]
---

# Employee Slate configuration for CBS

Core Business Suite provides two setup options for configuring Employee Slate as the default employee support portal. You can select any one according to your organizational requirement.

Starting with Core Business Suite Foundation version 3.0.5, Employee Slate is the default employee support portal.

The Employee Slate setup options are as follows:

-   Employee Slate for Moveworks
-   Employee Slate for Now Assist

**Note:**

Employee Slate for Moveworks is the recommended path as is mentioned in your instance in terms of overall capabilities. Only in situations where Employee Slate for Moveworks is not available, should you select the Employee Slate for Now Assist option.

If you configure both Employee Slate for Moveworks and Employee Slate for Now Assist, both options appear, each linking to its **Configuration Console**. The following table describes both options.

<table id="employee-slate-config-cbs-options-table"><thead><tr><th>

Option

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Employee Slate for Moveworks

</td><td>

An AI-enabled employee portal paired with the Moveworks conversational assistant. Provides a chat-first experience across the portal with broad self-service coverage. -   Use case: Organizations standardizing on a single AI assistant across channels.
-   Result: Personalized guidance per role across self-service interactions.
-   Prerequisites: Active Moveworks contract and integration setup.

</td></tr><tr><td>

Employee Slate for Now Assist

</td><td>

An AI-native employee portal with Now Assist. A fully native path with no external dependency. -   Use case: Organizations with no access to Moveworks.
-   Result: AI-assisted self-service across the employee portal with no external integration.
-   Prerequisites: Active Now Assist entitlement; no Moveworks contract or integration setup available.

</td></tr></tbody>
</table>To set up any option, install the application and set it up in your Configuration Console.

-   **[Configure Employee Slate for Moveworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/config-es-cbs-moveworks.md)**  
Configure Employee Slate for Moveworks to provide a conversational interface for employee portal queries on CBS. Use the Configuration Summary page to complete setup across five sections and export the finished configuration.
-   **[Configure Employee Slate for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/config-es-cbs-na.md)**  
Configure Employee Slate for Now Assist to provide a conversational interface for employee portal queries on CBS. Use the Configuration Summary page to complete setup across six sections and export the finished configuration.

**Parent Topic:**[Configure Core Business Suite Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/configure-cbs.md)

