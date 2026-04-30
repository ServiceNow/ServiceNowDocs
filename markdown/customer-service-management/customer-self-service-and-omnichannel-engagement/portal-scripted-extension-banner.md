---
title: Provide web page link buttons to display on the Portal Banner widget
description: Provide a link to a web page that you want to display by defining primary or secondary buttons on the Portal Banner widget. The widget displays these buttons by default.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Portal Banner widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Provide web page link buttons to display on the Portal Banner widget

Provide a link to a web page that you want to display by defining primary or secondary buttons on the Portal Banner widget. The widget displays these buttons by default.

## Before you begin

The UI Components for Customer Portals plugin must be installed. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md).

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  On the Extension Points page, in the API Name column, enter `*banner`.

3.  Select **sn\_ciwf\_ui\_cmpnt.BannerButtonsConditionScript** in the **API Name** column.

    If a message appears about the application scope, select **here** to be able to edit the record.

4.  On the BannerButtonsConditionScript page, in the Related links section, select **Create Implementation**.

    If a message appears about the application scope, select **here** to be able to edit the record.

5.  On the BannerButtonsConditionScript page, in the **Script** field, define the primary and secondary buttons by pasting the following CSS code and then customizing it.

    ```
    var BannerButtonsConditionScript = Class.create();
    BannerButtonsConditionScript.prototype = {
        initialize: function() {
        },
    
    	showPrimaryButton: function() {
    		// add your condition here
    		return true;
    	},
    
    	showSecondaryButton: function() {
    		// add your condition here
    		return true;
    	},
    
        type: 'BannerButtonsConditionScript'
    };
    ```

6.  Copy the name of the condition script from the **Name** field.

7.  Select **Update**.

8.  Navigate to your portal home page.

9.  On the Edit page, select the Portal Banner widget.

10. Press Control+right-click.

11. Select **Instance Options**.

12. In the **Behavior** section, paste the name that you copied into the **Button Condition Script** field.

13. Select the condition script from the list.

14. Select **Save**.


