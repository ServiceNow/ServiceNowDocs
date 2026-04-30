---
title: Configure a space details card
description: Configure a space card in the Location Directory, Kiosk Indoor Mapping, or Reservation by updating the card's template with the specific details that you want to customize. You can configure a new field, button, or style for each space card.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 1
breadcrumb: [Configure a workplace card, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure a space details card

Configure a space card in the Location Directory, Kiosk Indoor Mapping, or Reservation by updating the card's template with the specific details that you want to customize. You can configure a new field, button, or style for each space card.

## Before you begin

Role required: admin

## About this task

Card configuration allows you to customize the appearance and features of space cards. Choose the space card you wish to modify, and add a new field or button, or apply a style as needed.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Card configuration**.

2.  Select the **Default space card** for space cards.

    Cards are available for users, neighborhood, spaces, and rooms.

3.  Verify the application scope and edit the details.

4.  Open the WsdConfigurableSpaceCard Template and edit the record.

5.  In the XML script, insert a new HTML division \( &lt;div&gt;\) where you want the new field to appear.

    The following is the sample script for adding the usable\_size\_sq\_meter field.

    ```
    <div class="info-row" ng-if="data.usable_size_sq_meter">
    <div class="info-icon">
    <i class="fa fa-arrows-alt"></i>
    </div>
    <div class="info-text">{{ data.usable_size_sq_meter }}m square</div>
    </div>
    ```

6.  Save the record.

7.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

8.  In the Name column, search and select WSDConfigurableCardDataInjectcor.

9.  In the Script, add or update the function to ensure the new field is provided to the template.

    The following is the sample function for adding the usable\_size\_sq\_meter field.

    ```
    cards.forEach( function(card) {
    if (card.type ==='space') {
    var spaceGr.get(card.data.sysId)) {
    card.data.usable_size_sq_meter = spaceGr.getValue('usable_size_sq_meter');
    }
    }
    });
    
    ```

10. Navigate to the Location Directory and select the space where the new field has been added.

11. Confirm the new field appears in the space card.

    ![field details configuration on the space card.](../images/wsd-card-config-user.png)


**Parent Topic:**[Configure a workplace card](configure-workplace-card.md)

