---
title: Map functions with push actions on the actionable push notification
description: Associate functions to the actions in your notification so the instance uses the correct function for each action.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure actionable push notifications, Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Map functions with push actions on the actionable push notification

Associate functions to the actions in your notification so the instance uses the correct function for each action.

## Before you begin

Role required: admin

## Procedure

1.  **System Mobile** &gt; **Mobile Push Notifications** &gt; **Push Notifications**, and open the notification you created in previous steps.

2.  In the **Push Action Instances** related list, click **New**.

3.  In the Push action instance form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Push Notification|Push notification associated with this push action instance. This is automatically filled in with your push notification.|
    |Application|Scoped application associated with this record. This is automatically filled in with the current application.|
    |Push Action|Push action from your push notification record. Select one of the available actions.|
    |Button|Function to associate with the push action. Select an action you created in previous steps. This action will trigger when a user uses the action listed in the **Push Action** field.|

4.  Add a push parameter to your push action instance.

    If your push action receives a value from your user, you need to configure a push parameter to pass this value to your record. For example, if you create a reject action that requires your user to enter a reason for the rejection, the action must have a parameter to pass that text value to your approval record.

    1.  Verify that your push action requires a parameter. In the push action instance form, click the preview icon \(![Preview icon](../image/gac-info-icon.png)\) next to the **Push action** field. If the push action has a value of `Text Response` in the **Response type** field, you must create a push parameter.

        ![Push action with a response type of text response](../image/action-response-type.png)

    2.  Find the button parameter by clicking the preview icon \(![Preview icon](../image/gac-info-icon.png)\) next to the **Button** field.

    3.  In the function pop up click **Open record** to open the function form.

        ![Open record button on the function pop up](../image/open-function-record.png)

    4.  In the function form, note the parameter that appears in the **UI Parameters** related list at the bottom on the form. You will need this value in later steps.

    5.  Click the back button to return to the push action instance form.

    6.  In the **Push Parameter Values** related list, click **New**.

    7.  In the push parameter value form, select your parameter in the **Parameter** field. This is the parameter you noted from the function form in step d.

    8.  Click **Submit** to save your push parameter value.

5.  In the push action instance form, click **Submit**.


## Example

This example notification uses **accept-rejectwcomments-back** in the **Category** field. If you click the preview icon \(![Preview icon](../image/gac-info-icon.png)\), you can see that this category uses two actions: **Accept** and **Reject**.

![A push notification displaying a preview of the category record.](../image/action-push-example-1.png)

In the push action instance shown here, the `Approve` push action is selected in the **Push Action** field, and the `Approve REQ /w comments` function is selected in the **Button** field. The instance executes this function when a user taps the **Approve** button in their notification.

![Push action instance associating an action with a function](../image/action-push-example-2.png)

**Parent Topic:**[Configure actionable push notifications](../concept/actionable-push-notification.md)

