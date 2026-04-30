---
title: Create a service account and private key in Google Dialogflow ES
description: To use Google Dialogflow as your NLU provider for Virtual Agent, create a service account and private key for your agent in Google Dialogflow.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Service account, private key, Google Dialogflow ES, NLU, Virtual Agent]
breadcrumb: [Configure Google Dialogflow ES as the NLU provider for Virtual Agent, Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create a service account and private key in Google Dialogflow ES

To use Google Dialogflow as your NLU provider for Virtual Agent, create a service account and private key for your agent in Google Dialogflow.

## Before you begin

[Create an agent in Google Dialogflow.](https://cloud.google.com/dialogflow/es/docs/agents-manage)

Role required: admin

## Procedure

1.  Log in to your Google Dialogflow account.

2.  Select the agent settings icon, and then select the project ID on the **General** tab.

    ![Select settings, and then find the Google Project ID on the General tab.](../images/ggl-dialogflow-projectid.png)

3.  On the Google Cloud dashboard, select **Go to project settings**.

    ![On the Google Cloud Home dashboard, Go to project settings displays on the Project info card.](../images/ggl-dialogflow-go-project-settings.png)

4.  On the IAM &amp; Admin page, select **Service Accounts**.

5.  Select **+ Create Service Account**.

    ![When you select the Service Accounts option in the side menu, the Create Service Account option appears in the header bar.](../images/ggl-dialogflow-create-srvc-account.png)

6.  Provide a name, and then select **Create and Continue**.

7.  Under the Grant this service account access to project section, select **Owner** as the role.

    ![Select Owner from the Role list.](../images/ggl-srvc-acct-owner-role.png)

8.  Select **Continue**.

9.  Select **Done**.

10. In the **Email** column, select the link for the record.

    ![The Service accounts screen displays the email, name, and description. Select the Email address displayed in the column to open the Details page for the service account.](../images/ggl-dialogflow-srvc-account-record.png)

    The Service account details page opens.

11. Copy the Email and the Unique ID and save them for a later step.

    ![The email address and unique ID are displayed on the Details tab for the service account.](../images/ggl-srvacct-email-id.png)

12. On the Service account details page, select the **Keys** tab.

13. Select **Add Key** &gt; **Create new key**.

    ![The Add Key option is on the Keys tab for the service account.](../images/ggl-dialogflow-create-new-key.png)

14. When prompted for the key type, select **P12**, and then select **Create**.

    The P12 file is downloaded to your computer.

15. Make note of the private key password \(`notasecret`\).

    You will need this password in a [later step](vad-configure-dialogflow-security.md).

    ![The private key password is shown onscreen when you download the P12 file.](../images/ggl-p12-key-downloaded.png "Private key password example")


**Parent Topic:**[Configure Google Dialogflow ES as the NLU provider for Virtual Agent](../concept/configure-dialogflow-es-integration.md)

**Previous topic:**[Configure Google Dialogflow ES as the NLU provider for Virtual Agent](../concept/configure-dialogflow-es-integration.md)

**Next topic:**[Generate a Java Keystore \(JKS\) file and configure security on your ServiceNow instance](vad-configure-dialogflow-security.md)

