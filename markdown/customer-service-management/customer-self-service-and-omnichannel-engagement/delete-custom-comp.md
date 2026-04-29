---
title: Delete a custom component
description: Delete a component to remove a custom component and all its instances from the Web Embeddables application and websites. You can only delete custom components that are in a deactivated state. Once deleted, the custom components can’t be restored.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update or create web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Delete a custom component

Delete a component to remove a custom component and all its instances from the Web Embeddables application and websites. You can only delete custom components that are in a deactivated state. Once deleted, the custom components can’t be restored.

## Before you begin

You must create a custom component. For more information, see [Create a custom component](create-custom-comp.md).

Role required: sn\_embeddable\_core.emb\_admin

## About this task

Deleting a component is a permanent and irreversible action. When you delete a component, the following events occur:

-   The component is removed from the Web Embeddables application.
-   All component instances of the component embedded in your modules are deleted.
-   Any embed code associated with these instances becomes non-functional on your webpages, and results in broken or missing content where the component was previously displayed.

This action cannot be undone. Before proceeding, review all dependencies and confirm that the component is no longer required in any module or webpage.

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the Manage components section, select Action \(⋮\) on the component.

3.  Select **Delete**.

    **Note:** A dialog box appears for confirmation. Review the information.

4.  Select **Delete**.

    **Note:** A confirmation message appears `Component is now inactive and its existing instances may become hidden on your websites.`


## Result

The custom component and its instances disappear from the **Manage components** section on the Web Embeddables application homepage and the website where it’s embedded.

