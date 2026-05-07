---
title: Create a custom component
description: Create a custom component to present information, capture user input, or offer interactive functionality on a third party website. You can also clone the existing component and customize it.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update or create web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Create a custom component

Create a custom component to present information, capture user input, or offer interactive functionality on a third party website. You can also clone the existing component and customize it.

## Before you begin

-   Beginning with the Zurich release, Component UI Builder is enabled by default in your instance.
-   Existing customers on release versions before Zurich release, you must enable Component UI Builder in your instance by activating UI Builder plugin \(sn\_ui\_builder\) to create a custom component.
-   Make sure you’re referring UI Builder version 27.2 or above for component creation.
-   Ensure the \[sn\_cb\_experiences.uib.enable.cb\] system property is set to true.

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embedabbles** &gt; **Homepage**.

2.  In the Manage components section, select **Create component**.

3.  Enter the following field values.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the custom component.|
    |Component tag suffix|Enter a unique value to append to the prefix of component tag. It can’t be edited later.|
    |Component tag|The tag used in the embed code helps identify the component.|
    |Description|Description of your component.|
    |Icon|Thumbnail image of the custom component.|

4.  Select **Create component**.

    The UI Builder application opens in a new browser tab in embeddable mode, where you can customize the component.

5.  In a blank canvas, select **Add content**.

    **Note:** Component palette displays components that are eligible to embed. Make sure the embed-ready category is selected.

6.  Select the component.

7.  Configure the component properties.

8.  Select component from the other category.

    **Note:** If you select any other category, make sure added component meets the criteria for embedding components on third-party websites.

9.  Save the changes.

10. Select the **Configure embeddable** to navigate back to the Web Embeddables app homepage.


## Result

The custom component is created and shown under the **Manage components** section on the Web Embeddables app home page and is identified by the **Custom** label.

