---
title: Hide or show categories in the Data List widget
description: Create a condition script to hide or show a category in the Portal Data List widget.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Portal Data List widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Hide or show categories in the Data List widget

Create a condition script to hide or show a category in the Portal Data List widget.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see[Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md)

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **System Extensions Points** &gt; **Scripted Extensions Points**.

2.  On the Extension Points page, in the **API Name column** search field, enter `*datalist`.

3.  Select the **sn\_ciwf\_ui\_cmpnt.DatalistCategoryConditionScript** in the **API Name** column.

    If a message appears about the application scope, select **here** to be able to edit the record.

4.  On the DatalistCategoryConditionScript page, in the Related links, select **Create implementation**.

5.  In the **Script** field, paste the following CSS code:

    ```
    showCategory: function(category_id) { 
    
          /* 
    
          if(category_id=="cases_category"){ 
    
              return true; 
          } 
    
          */ 
    
          return true; 
    
        }
    ```

6.  Copy the name of a condition script from the **Name** field.

7.  Select **Update**.

8.  Navigate to your portal home page.

9.  On the Data List widget, press Control+right-click.

10. Select **Instance Options**.

11. In the Behavior section, paste the name that you copied into the **Categories condition script** field.

12. Select the condition script from the list.

13. Select **Save**.


