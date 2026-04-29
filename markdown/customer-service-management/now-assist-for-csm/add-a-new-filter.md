---
title: Add a new filter
description: Add a new filter to a UI Builder dashboard to enable users to refine data views based on additional fields such as consumer, product, or other custom fields.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Generative AI, Generative AI for Customer Service Management, Generative AI for customer service agents]
breadcrumb: [Trending topics dashboard, Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Add a new filter

Add a new filter to a UI Builder dashboard to enable users to refine data views based on additional fields such as consumer, product, or other custom fields.

## Before you begin

Role required: admin or maint

If the Components tab in UI Builder is not available, run provided background script to enable the component view for maint users.

```
var gr = new GlideRecord('sys_properties'); 
gr.setValue("sys_scope", "e9b68250cdffe4e1c64e494026ec6e9a"); 
gr.setValue("name", "sn_cb_experiences.uib.enable.cb"); 
gr.setValue("write_roles", 'maint'); 
gr.setValue("value", "true"); 
gr.insert(); 
```

## About this task

Filters allow users to refine dashboard data by specific fields. This procedure demonstrates how to add a new filter to any base system dashboard such as trending topics dashboard or sentiment analysis dashboard by duplicating and configuring an existing filter carousel item.

## Procedure

1.  Navigate to **All** &gt; **UI Builder** and select a UIB component.

2.  Under **Components** tab search for the corresponding component.

    The different UI Builder Component names:

    -   Trending topics dashboard: OOB Trending Topics Dashboard, Top Trends, Trending topics by Field Insight \(accounts, products, assignment group, channels\), OOB Topic Details Dashboard, Topic Over Time Visualization, Topic Breakdown Visualization, Topic Affected Regions Visualization.
    -   Sentiment analysis dashboard: OOB Sentiment Analysis Dashboard, Sentiment Over Time Visualization, Sentiment Breakdown Visualization, Sentiment Top Drivers Insight \(Negative sentiment and Positive sentiment drivers\), Sentiment by Assignment Group Insight, Sentiment After Escalation Insight, Sentiment by Channel Insight.
    If working with the base system component, create a clone before making modifications.

3.  Select a **Filter Carousel Item 2** in the component tree.

4.  [Duplicate the component](https://www.servicenow.com/docs/access?context=duplicate-components&version=australia&pubname=australia-application-development&ft:locale=en-US) from the context menu.

    Drag the duplicated filter to reorder it as needed within the carousel.

5.  Select the newly created filter in the left panel.

    The configuration panel displays on the right side.

6.  Under **Filter source**, change the **Table** name to **Trending topic record**.

7.  Change the **Field** to your desired field.

    For example, enter **Consumer**.

8.  Select **Apply**.

9.  Under **UI element**, change the **Filter label** field to match your desired field name.

    For example, enter **Consumer**.

10. Rename the component ID to match the field using lowercase and dashes.

    For example, enter **filter\_consumer**

11. Copy this ID to the clipboard for use in subsequent steps.

12. Select **Apply**.

13. Select **Save**.

14. In the top left of the screen, open the hamburger menu and select **Open component record**.

15. In the **Composition** section, search for your component ID.

16. Open the search function using Cmd+F \(Mac\) or Ctrl+F \(Windows\).

17. Paste the component ID from step 10 using Cmd+V \(Mac\) or Ctrl+V \(Windows\).

18. Press Return \(Mac\) or Enter \(Windows\) to search.

19. Open the search function again using Cmd+F \(Mac\) or Ctrl+F \(Windows\).

20. Enter **filterId** in the search box.

21. Press Return \(Mac\) or Enter \(Windows\) to perform the search.

22. Locate the **value** field under the filterId property.

23. Change the final value to the filterId from step 10.

    For example, enter **filter\_consumer**. The filterId can be any unique value.

24. Select **Update** to save.

    The new filter is now configured and ready to use on the dashboard.


## Result

The new filter appears in the dashboard filter carousel and enables users to filter data by the specified field.

**Important:** If you plan to make additional changes to the original component, refresh the UI Builder component page to prevent losing the changes made in steps 6-10.

**Related topics**  


[Change graph visualization](change-graph-visualization.md)

[Change an insight to use a different field for trending topics](change-insight-to-use-a-different-field.md)

