---
title: Enable the display of the Microsoft Viva card in Microsoft SharePoint
description: Enable the display of the Microsoft Viva card details to be displayed to users in Microsoft SharePoint.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Employee Center for Microsoft Viva Connections, Employee Center for Microsoft Viva Connections, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Enable the display of the Microsoft Viva card in Microsoft SharePoint

Enable the display of the Microsoft Viva card details to be displayed to users in Microsoft SharePoint.

## Before you begin

Role required: SharePoint administrator

## About this task

The Microsoft Viva card provides users with a quick view of all tasks assigned to them in both Microsoft SharePoint and Microsoft Teams. It also enables users to quickly navigate to Employee Center to view detailed tasks there.

First grant app access in Microsoft SharePoint and then publish the card.

## Procedure

1.  Log in to Microsoft SharePoint admin center.

2.  Grant app access to the Microsoft Viva integrations app access in Microsoft SharePoint.

    1.  Navigate to **Advanced** &gt; **API access**.

    2.  Navigate to **Pending requests** &gt; **Organization-wide**.

    3.  Select **Employee Experience integration with Viva**.

    4.  Select **Approve**.

3.  Publish the card.

    1.  Select **Edit**.

    2.  Select **Add a card**.

    3.  Select the **ServiceNow Viva Integrations** card.

    4.  Hover over the card and select the Edit icon \(![Edit icon](../../human-resources/image/edit-new.png)\).

    5.  On the form, fill in the fields.

        For more information, see [Microsoft Viva integrations card properties](../reference/viva-card-properties.md).

    6.  Select **Republish**.

        The card is now available for use.


**Parent Topic:**[Managing Employee Center for Microsoft Viva Connections](../concept/manage-viva.md)

