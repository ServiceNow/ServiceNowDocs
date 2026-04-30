---
title: Installing Conversational Integration with Google chat
description: Install the Google chat \(sn\_va\_google-chat\) application so that Now Virtual Agent and Google chat users can interact with each other.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-06-23"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Google chat, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Installing Conversational Integration with Google chat

Install the Google chat \(sn\_va\_google-chat\) application so that Now Virtual Agent and Google chat users can interact with each other.

## Before you begin

-   Roles required:

    -   virtual\_agent\_admin and external\_app\_install\_admin or admin.

    -   Google chat administrator \(one of the following\): Global administrator, Application administrator, or Cloud Application administrator.

## Procedure

1.  On the Google workspace, navigate to [Build a Google Chat app with Google Apps Script](https://developers.google.com/workspace/chat/quickstart/apps-script-app).

2.  Verify that you have fulfilled the prerequisites.

3.  Follow the instructions in the Open your Cloud project in the Google Cloud console section.

4.  Follow the instructions in the Turn on the Chat API section.

5.  Navigate to [https://console.cloud.google.com/](https://console.cloud.google.com/).

6.  Select **APIs &amp; Services** from the Quick Access view or from the side menu.

7.  In the list of APIs, select **Google Chat API**.

8.  On the Google chat API screen, select the **Configuration** tab.

9.  Verify **Build this Chat app as a Workspace add-on** is selected.

10. Complete the Application info fields:

    |Field|Description|
    |-----|-----------|
    |App name|Application name.|
    |Avatar URL|Publicly accessible avatar image for the application.|
    |Description|Application description.|

11. In the Interactive features section, verify **Enable interactive features** is selected.

12. In the Connection Settings section, select **HTTP endpoint URL**.

13. In the Triggers section, select **Use a common HTTP endpoint URL for all triggers**.

14. In the HTTP endpoint URL field, enter the instance name and the URL extension: `<instance url>/api/sn_va_google_chat/va_google_chat_inbound/events`.

15. In the Visibility section, select **Make this Chat app available to specific people and groups in servicenow.**

16. In the Enter email addresses to add individuals and groups in your domain field, enter your email address.

17. Select **Save**.

18. Scroll back to the top of the screen.

19. In the Connection settings section, find and note the Service Account Email - this is your Inbound Service Account Email.

20. In the side menu, navigate to Credentials.

21. In the Service Accounts section, select **Manage service accounts**.

22. Select **+ Create service account**.

23. On the Create service account screen, fill out the fields:

    |Field|Description|
    |-----|-----------|
    |Service account name|Name for the service account.|
    |Service account ID|This will be automatically generated for you.|
    |Service account description|Description for the service account.|

24. Find and note the email account under the Service account ID field - this is your Outbound Service Account email.

25. Select **Done**.

26. On the Service Accounts screenn,navigate to the Manage Keys page and select your new outbound service account.

27. Select the Keys tab.

28. From the Add Key drop-down list, select **Create new key**.

29. On the Create private key for 'Outbound Service Account' window, select **P12**.

30. Select **Create** - this automatically downloads a file to your machine.

31. On the Private key saved to your computer window, enter a private key password.


## What to do next

[Integrating Virtual Agent with Google chat](integrating-va-google-chat.md)

**Parent Topic:**[Conversational Integration with Google chat](../concept/gchat-conv-integration.md)

