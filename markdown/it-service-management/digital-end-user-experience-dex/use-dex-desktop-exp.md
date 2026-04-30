---
title: Use DEX Desktop Assistant
description: Use DEX Desktop Assistant to get quick access to self-service and diagnostic tools, notifications about outages and announcements, and support resources.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Use DEX Desktop Assistant

Use DEX Desktop Assistant to get quick access to self-service and diagnostic tools, notifications about outages and announcements, and support resources.

The DEX Desktop Assistant provides a dedicated communication interface for employees, enabling access to self-service options, IT notifications, and support resources.

Desktop Assistant facilitates streamlined workflows by enabling employees to perform network diagnostics, access IT catalogs, use the ServiceNow® Employee Center, and interact with virtual agents for assistance. IT teams can use the tool to issue outage notifications or critical announcements, promoting timely communication and efficient support delivery.

<table id="table_r2b_mxq_lwb"><thead><tr><th>

Components

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header

</td><td>

The Desktop Assistant header includes the following:

-   Application name
-   Virtual agent or chat icon ![](../image/icon-virtual-agent.png): Selecting this icon opens a chat-based Virtual Agent interface that uses Now Assist to provide help, answers, and support.
-   Notification icon ![](../image/icon-notification-bell.png): This icon displays a red dot with a number to indicate the number of new notifications. Selecting the icon displays the list of notifications.
-   User profile icon ![](../image/icon-user-login.png): Selecting this icon enables you to log out of Desktop Assistant.

</td></tr><tr><td>

Sections

</td><td>

Sections help you search for items by arranging them sequentially and in logical groups. By default, ServiceNow provides the My resources and Quick links sections.

 Desktop Assistant administrators can configure additional sections for the home page. For more information, see [Add a section in the Desktop Assistant home page](../task/add-home-page-section.md).

</td></tr><tr><td>

Cards

</td><td>

Desktop Assistant provides the following cards with the base system:-   Device health check: Monitor and self-resolve common device health issues. For more information, see [Check device health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md).
-   Network test: Run network diagnostic tests. For more information, see [Test network connectivity of your device](../task/test-internet-connection.md).
-   Employee Center: Access the Employee Center portal. For more information, see [Open Employee Center from Desktop Assistant](../task/open-employee-center.md).
-   Outages: View outages on Employee Center. For more information, see [View outages from Desktop Assistant](../task/open-outages.md).

By default, the Device health check and Network test cards are mapped to the My resources section and the Employee Center and Outages cards are mapped to the Quick links section. Desktop Assistant administrators can map or remove cards from any section on the home page. For more information, see [Map a card to a section](../task/map-card-section.md) and [Delete a card from the Desktop Assistant home page](../task/delete-card.md).

</td></tr></tbody>
</table>**Note:** If you experience issues with Desktop Assistant, troubleshoot them by accessing the logs at these locations:

-   macOS: `Users/[username]/Library/Application Support/desktop_assistant_app/logs`
-   Windows: `Users\[username]\AppData\Roaming\desktop_assistant_app\logs`

