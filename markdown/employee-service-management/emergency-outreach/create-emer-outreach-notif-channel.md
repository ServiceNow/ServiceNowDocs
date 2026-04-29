---
title: Create an Emergency Outreach notification channel
description: Create a notification channel to send health status requests using your company's preferred communication method, such as the Slack or Microsoft Teams collaboration platforms. Create the notification channel using a script or a subflow.
locale: en-US
release: australia
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Emergency Outreach notifications, Emergency Outreach, Emergency Response Management, Employee Service Management]
---

# Create an Emergency Outreach notification channel

Create a notification channel to send health status requests using your company's preferred communication method, such as the Slack or Microsoft Teams collaboration platforms. Create the notification channel using a script or a subflow.

## Before you begin

Role required: sn\_imt\_checkin.checkin\_admin or admin

## About this task

After you create a notification channel, you can select the channel when sending a notification. The channel uses the specified subject and body, and sends notifications to the users that you select when you send the health status request.

For example, your company's IT network group has a Slack channel that they monitor more closely than email. Create a Slack notification channel. To communicate with IT network group members, select the group as the target audience and select the Slack notification channel.

If the **Email notification** and **Now Mobile Push notification** check boxes are selected, all three notifications are sent. To use only the Slack notification channel, clear these two check boxes.

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Channels**.

2.  Click **New**.

    ![New channel record with the script option selected and default script.](../image/emer-outreach-notif-channel.png)

3.  Enter the name of your notification channel.

    Use a short name that indicates the communication method to make it easy for the requester to pick the correct channel.

4.  In the **Subject** field, enter the subject of your notification channel.

5.  In the **Body** field, enter the body message.

6.  Create a script notification channel.

    1.  In the **Notification type** field, leave the default notification type of **Script**.

    2.  In the **Script** field, replace the code in the comment with the script to connect to your channel.

        ```
        {
                    // sendNotification(responses.acknowledgementsGr.user.email, 
        channelGr.subject, channelGr.body);
                }
        ```

        For information about JavaScript APIs for GlideRecord, see [GlideRecord - Scoped](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    3.  Click **Submit**.

    The following example includes code to count the number of acknowledgements and survey instances generated when the notification is sent. It displays the number of acknowledgements and survey instances that succeeded. Use this information to review and handle errors that appear in the Delivery Log related list in the Outreach record.

    ```
    (function notify(responses, channelGr) {
        var record = responses.mode === 'acknowledgements' 
            ? responses.acknowledgementsGr 
            : responses.surveyInstancesGr;
        var totalCount = record.getRowCount();
        var numSent = 0;
        while (record.next()) {
            try {
                // sendNotification(record.user.email, channelGr.subject, channelGr.body)
                numSent += 1;
            } catch (err) {
                gs.error('Error occurred: ' + err.message);
            }
        }
        return { total_count: totalCount, sent_count: numSent };
    })(responses, channelGr);
    ```

7.  Create a subflow notification channel.

    1.  Create a subflow to use in the outreach notification.

        For information about creating, publishing, and testing subflows, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

        Use the following inputs in the subflow that you create:

        -   *mode* \(string\)
        -   *akcnowledgements* \(Records of sn\_imt\_checkin\_check\_in\_acknowledgement\)

            If the mode is *acknowledgements*, then acknowledgements are set to a valid GlideRecord and *survey\_instances* is `null`.

        -   *survey\_instances* \(Records of asmt\_assessment\_instance\)

            If the mode is *survey\_instances*, then survey\_instances is set to a valid GlideRecord and *acknowledgements* is `null`.

        -   *channel* \(Reference of sn\_imt\_checkin\_channels\)
        The following outputs are optional:

        -   *total\_count* \(integer\)
        -   *sent\_count* \(integer\)
        To review these outputs, include the number of total acknowledgements or surveys versus the successful acknowledgements or surveys.

    2.  Select the **Subflow** notification type.

        The Script section changes to Flow, and the **Subflow** reference field appears.

    3.  Select the subflow that you created.

8.  Click **Submit**.


When an outreach is sent using a custom notification channel, a Delivery Logs related list appears in the Outreach message.

![Delivery logs related list showing a failed log status.](../image/outreach-delivery-log-list.png "Delivery logs related list")

1.  Test the notification channel for an outreach message, and open the failed record to review the error message.
2.  Fix errors that caused the notification to fail.
3.  Continue testing the notification channel until it no longer fails.

## Slack channel script

**Note:** The following script is for reference only. Refer to it when you develop a notification channel script for your environment.

```
(function notify(responses, channelGr) {
    var createClient = function () {
        var client = new sn_ws.RESTMessageV2();      
        client.setRequestHeader('Authorization', 'Bearer xoxb-222222222222-1111111111111-000000000000000000000000');
        client.setRequestHeader("Accept", "application/json");
        client.setRequestHeader('Content-type', 'application/json');
        return client;
    };

    var getEmailToSlackIdMap = function (users) {
        var emailToSlackIdMap = {};
        for (var i = 0; i < users.length; i++) {
            var email = users[i].profile.email;
            if (email) {
                emailToSlackIdMap[email] = users[i].id;
            }
        }
        return emailToSlackIdMap;
    };

    var runSlackCommand = function (method, params) {
        var client = createClient();
        client.setHttpMethod('post');
        client.setEndpoint('https://slack.com/api/' + method);
        client.setRequestBody(JSON.stringify(params));
        var response = client.execute();
        if (response.getStatusCode() < 200 || response.getStatusCode() > 299) {
            throw new Error('Failure running ' + method + ':\n' + response.getBody());
        }

        var body = JSON.parse(response.getBody());
        if (!body.ok) {
            throw new Error(body.error);
        }

        return body;
    };

    var sendMessage = function (userId, message) {
        var openConversationResponse = runSlackCommand('conversations.open', { users: userId });
        var channel = openConversationResponse.channel.id;
        runSlackCommand('chat.postMessage', { channel: channel, text: message });
    };

    var users = runSlackCommand('users.list').members;
    var emailToSlackIdMap = getEmailToSlackIdMap(users);
    var body = channelGr.getValue('body') || '<p></p>';
    var record = responses.mode === 'acknowledgements' ? responses.acknowledgementsGr : responses.surveyInstancesGr;
    var numSent = 0;

    while (record.next()) {
        var email = record.user.email + '';

        var link = responses.mode === 'acknowledgements'
            ? gs.getProperty('glide.servlet.uri') + record.getLink(true)
            : gs.getProperty('glide.servlet.uri') + 'sp?id=take_survey&instance_id=' + record.getUniqueValue();

        var message = body + '\n' + link;

        var slackId = emailToSlackIdMap[email];
        if (slackId) {
            sendMessage(slackId, message);
            numSent += 1;
        }
    }

    return { sent_count: numSent };
})(responses, channelGr);
```

