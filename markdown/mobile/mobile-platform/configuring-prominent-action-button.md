---
title: Configuring a prominent action button
description: Configure a prominent action button for quick access to Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/configuring-prominent-action-button.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configuring a prominent action button

Configure a prominent action button for quick access to Now Assist.

## Before you begin

Role required: admin

**Note:** You can only have one prominent action button per app type.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

2.  Select **New** to create a new button instance.

3.  Complete the following fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of the button.|
    |**Description**|Additional information about the button.|
    |**Parent**|The button's app type.|
    |**Application**|The application in which your button resides. This field is auto-populated.|
    |**Parent table**|Table where the button gets its data. Select the **Mobile app config \[sys\_sg\_native\_client\]** table.|
    |**Function**|Function used by this button instance.|
    |**Label**|Label that displays for the button.|
    |**Location**|The place where the button will reside. Select **Prominent Action**.|
    |**Icon**|Icon used to represent your button.|
    |**Order**|The order in which the button appears on the screen compared to other buttons.|
    |**Active**|Select whether the button is active or not.|

4.  Configure a badge count by navigating to the **sys\_sg\_badge\_count** table and setting your **Location** to **Prominent Action Button**.

5.  Select **Submit** to save your button.


**Parent Topic:**[Configuring Now Assist for Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configuring-now-assist-mobile.md)

