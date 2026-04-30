---
title: Reuse push notifications across mobile apps
description: Reuse push notifications across mobile apps with Mobile App Builder \(MAB\). Push notifications are configurable pushed messages that appear directly in mobile apps. Using MAB to manage push notifications streamlines your mobile application development into one tool.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Reuse push notifications across mobile apps

Reuse push notifications across mobile apps with Mobile App Builder \(MAB\). Push notifications are configurable pushed messages that appear directly in mobile apps. Using MAB to manage push notifications streamlines your mobile application development into one tool.

## Before you begin

Role required: admin

## About this task

This task describes how to reuse a push notification from one mobile app to another using MAB. For more information about MAB, see [Mobile App Builder](../concept/mab-concept.md).

To create a push notification from scratch, see [Mobile push notifications](../concept/sg-mobile-push-notifications.md).

In MAB, mobile notifications aren’t tied to a specific application scope and don't change based on the application scope you’re using. You can reuse push notifications that contain workflows from other ServiceNow® mobile applications and then use MAB to update records so they point to the correct app.

For example, if you have a push notification configured for Now Mobile, the standard ServiceNow Request Application, you can reuse this push notification with another mobile app. To reuse it, select the push notification record and configure it to point to your new mobile app as described in the following steps.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Mobile notifications** from the menu.

4.  From the **Mobile Applications** list, select the mobile app that contains the push notification you want to reuse in another app.

5.  From the **Push notification** events list, select the push notification event that contains the push notification you want to reuse.

    If you see the message **Edit in original scope** at the top of the page, select it to switch to the correct application scope.

6.  Make sure that the **Push notification event** is selected in the menu and do the following:

    1.  Scroll down to the **Mobile push application** section and select **Choose**.
    2.  In the **Choose an item** dialog box, select the mobile app where you want to reuse the push notification.
    3.  Select **Apply** and then select **Save**.
    Doing this step adds your mobile app to the list of mobile apps where this event applies.

    **Important:**

    You must still create or modify two records to apply this change:

    -   The push notification message.
    -   The message content records that must point to the same mobile application you just added to the event.
    If you don't want to remove the push notification from the original app, but want to reuse the push notification in your mobile app, you must do the following:

    -   Duplicate the **Push notification message** and message content records.
    -   Then target them to the matching mobile push application you just added to this event.
7.  In the menu, select the **Push notification message**.

    ![Push notification message selected in the Mobile App Builder menu](../image/mab-push-notif-message.png)

8.  With **Push notification message** selected in the navigation menu, do the following:

    1.  If necessary, select **Edit in original scope** at the top of the form.

    2.  Select the more options menu \(![More options menu icon](../image/button-more-ios.png)\).

    3.  Then select **Duplicate**.

    ![Mobile App Builder UI showing how to duplicate a push notification message.](../image/mab-duplicate-push-notif-msg.png)

9.  In the Create a push notification message dialog box, select **Create**, and then select **Go to Record** in the Success! pop-up window.

10. In the copy of the PUSH NOTIFICATION MESSAGE form Settings section, you must change the value of **Application to push a notification** to point to your application.

    For example, if you want to reuse the push notification from the ServiceNow Agent mobile app \(ServiceNow Mobile Application\) in the Now Mobile app \(ServiceNow Request Application\), select that value in the list as shown in the following:

    ![Mobile App Builder UI showing the new app being selected to reuse the push notification message.](../image/mab-push-not-msg-new-app.png)

11. Select **Save**.

12. Select the **Push notification message content** record in the navigation menu.

13. On the PUSH NOTIFICATION MESSAGE CONTENT record, in the **Push application** section, select the application that you chose in the Push notification message record:

    ![Mobile App Builder UI showing selection of application to reuse the push notification message content.](../image/mab-push-not-content-nuapp.png)

    **Important:** If you have any deep links in the **Push message content** script, the mobile app call used by the deep link generator must be changed to point to the application that you specified in the **Push app** field. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).

14. Select **Save**.

15. Finally, navigate back to the push notification event record from Step 5 \(by navigating back to the **Mobile notifications** tab from the categories menu\) and do the following:

    Add your new push notification message record in the **What push message to send** section.

    **Note:** If necessary, select **Edit in original scope** at the top of the form to add your new message record.


## What to do next

To verify that you have added this push notification to your mobile app, do the following:

1.  Navigate to the home screen in MAB.
2.  Select **Mobile notifications**.
3.  From the **Mobile applications** list, select the mobile app that you added the push notification to.

    If you have successfully added the event to your mobile app, you can see it in the **Push notifications** list.

    ![Mobile App Builder UI showing the reused push notification has been added to the new app.](../image/mab-push-not-verification.png)


If this event record's mobile push application matches that of an associated according to the chart below, you have completed the configuration.

|Mobile application|Mobile Push application|Push application name|Mobile app call for deeplinks|
|------------------|-----------------------|---------------------|-----------------------------|
|Now Mobile®|ServiceNow Request Application|SkyNowRequestPushApp|Requestor|
|Mobile Agent|ServiceNow Mobile Application|SkyNowPushApp|Agent|

**Parent Topic:**[Mobile push notifications](../concept/sg-mobile-push-notifications.md)

