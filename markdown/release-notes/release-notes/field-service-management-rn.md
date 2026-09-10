---
title: Field Service Management release notes
description: The ServiceNow Field Service Management application automates processes, enhances communication, and transforms field service delivery with AI-powered workflows to resolve customer needs efficiently, transparently, and proactively. Field Service Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Field Service Management release notes

The ServiceNow® Field Service Management application automates processes, enhances communication, and transforms field service delivery with AI-powered workflows to resolve customer needs efficiently, transparently, and proactively. Field Service Management was enhanced and updated in the Yokohama release.

## About Field Service Management

-   Define configurable rules that you can use to derive recommendation scores and optimize your appointment booking slots.
-   Create advanced dependency relationships among tasks to enhance scheduling accuracy.
-   Optimize your task assignments by using dependencies that align with the overall objectives and constraints of your resource allocation.
-   Streamline your capacity and resource management by using enhanced visualization in the Capacity Console.
-   Calculate the work duration for a work order task more accurately by using the Agent Efficiency feature.

See [Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/fsm-application-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Field Service Management is a ServiceNow AI Platform feature that is active by default.

    Leverage advanced features of Appointment Booking, such as the appointment slot recommendation, by activating the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin.

    Define the task dependencies for a work order task and schedule tasks based on the dependency by activating the Field Service Task Dependencies \(com.snc.fsm\_task\_dependency\) plugin.

    Integrate agent efficiency metrics with Field Service Management to define and use the efficiency of agents to estimate the work duration for tasks by activating the FSM Agent Efficiency \(com.snc.fsm\_agent\_efficiency​\) plugin.

-   **Upgrade information**
    -   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
    -   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

-   **[ServiceNow Otto for Field Service Management \(FSM\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-for-fsm-rn.md)**  
The ServiceNow® ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Yokohama release.

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/new-features-changes.md)

