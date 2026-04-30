---
title: Create a custom Emergency Outreach notification channel
description: Create a custom Emergency Outreach notification channel to send privacy consent requests using your company's preferred communication method, such as the Slack or Microsoft Teams collaboration platforms. Create the notification channel using a script or a subflow.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up data privacy consent settings for Contact Tracing, Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a custom Emergency Outreach notification channel

Create a custom Emergency Outreach notification channel to send privacy consent requests using your company's preferred communication method, such as the Slack or Microsoft Teams collaboration platforms. Create the notification channel using a script or a subflow.

## Before you begin

Role required: sn\_imt\_checkin.checkin\_admin or admin

## About this task

After you create a notification channel, you can select it when sending a notification. The channel uses the specified subject and body, and sends notifications to the users that you select when you send the privacy consent request.

For example, if your company's IT network group has a Slack channel that they monitor more closely than email, you could create a Slack notification channel. To communicate with IT network group members, you would select the group as the target audience and select the Slack notification channel.

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Channels**.

2.  Click **New**.

    ![New channel record with the script option selected and a default script.](../image/outreach-notif-channel-privacy.png)

3.  Enter the name of your notification channel.

    Use a short name to indicate the communication method so requesters can easily pick the correct channel.

4.  In the **Subject** field, enter the subject of your notification channel message.

5.  In the **Body** field, enter the body of the message.

6.  Create a script for the notification channel.

    1.  In the **Notification type** field, leave the default notification type of **Script**.

    2.  In the **Script** field, replace the code in the comment with the script to connect to your channel.

        ```
        {
                    // sendNotification(responses.privacyGr.user.email, 
        channelGr.subject, channelGr.body);
                }
        ```

        For information about JavaScript APIs for GlideRecord, see [GlideRecord - Scoped](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

    3.  Click **Submit**.

    The following example includes code to count the number of privacy consent requests generated when the notification is sent. It displays the number of privacy consent requests that were delivered successfully. Use this information to review and handle errors that appear in the Delivery Log related list in the Outreach record.

    ```
    (function notify(responses, channelGr) {
    	var totalCount = responses.privacyGr.getRowCount();
        var numSent = 0;
        if (responses.mode === 'privacy_consent') {
            while (responses.privacyGr.next()) {
                try {
                    // sendNotification(record.user.email, channelGr.subject, channelGr.body)
                    numSent += 1;
                } catch (err) {
                    gs.error('Error occurred: ' + err.message);
                }
            }
        }
        return {
            total_count: totalCount,
            sent_count: numSent
        };
    })(responses, channelGr);
    ```

7.  Create a subflow notification channel.

    1.  Create a subflow to use in the notification.

        For information about creating, publishing, and testing subflows, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

        Use the following inputs in the subflow that you create:

        -   *mode* \(string\)
        -   *Privacy Consent* \(Records of sn\_imt\_tracing\_user\_privacy\_consent\)

            If the mode is *Privacy Consent*, then acknowledgements are set to a valid GlideRecord and *survey\_instances* is `null`.

        -   *channel* \(Reference of sn\_imt\_checkin\_channels\)
        The following outputs are optional:

        -   *total\_count* \(integer\)
        -   *sent\_count* \(integer\)
        To review these outputs, include the number of total privacy consent requests versus the successful privacy consent requests.

    2.  Select the **Subflow** notification type.

        The Script section changes to Flow, and the **Subflow** reference field appears.

    3.  Select the subflow that you created.

8.  Click **Submit**.


When a notification is sent using a custom notification channel, a Delivery Logs related list appears in the Outreach message.

![Delivery logs related list showing a failed log status.](../../business-continuity/image/outreach-delivery-log-list.png "Delivery logs related list")

1.  Test the notification channel for an outreach message.
2.  Open any failed channel record to review the error messages and fix errors that caused the notification to fail.
3.  Continue testing the notification channel until the channel no longer fails.

**Parent Topic:**[Setting up data privacy consent settings for Contact Tracing](../concept/set-up-privacy-consent-settings.md)

