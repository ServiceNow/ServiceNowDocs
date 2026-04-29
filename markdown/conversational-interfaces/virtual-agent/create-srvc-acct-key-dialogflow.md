---
title: Create a service account and private key for the Google Dialogflow project
description: To use Google Dialogflow with Virtual Agent Bot Interconnect, the second step is to create a service account and private key for the new agent in Google Dialogflow.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a service account and private key for the Google Dialogflow project

To use Google Dialogflow with Virtual Agent Bot Interconnect, the second step is to create a service account and private key for the new agent in Google Dialogflow.

## Before you begin

Role required: admin

## Procedure

1.  On the project dashboard page, click **Go to project settings**.

    ![On the Google Cloud Home dashboard, Go to project settings displays on the Project info card.](../images/ggl-dialogflow-go-project-settings.png)

2.  On the IAM &amp; Admin page, click **Service Accounts**.

3.  Click **+ Create Service Account**.

    ![When you select the Service Accounts option in the side menu, the Create Service Account option appears in the header bar.](../images/ggl-dialogflow-create-srvc-account.png)

4.  Provide a name, and then click **Create and Continue**.

5.  Under Select a role, select **Dialogflow** &gt; **Dialogflow API Client**.

6.  Click **Continue**.

    ![Assign the Dialogflow API Client role on the service account details screen, then click Continue to go to the next step.](../images/ggl-dialogflow-assign-role.png)

7.  Click **Done**.

8.  Click the link for the record in the **Email** column.

    ![The Service accounts screen displays the email, name, and description. Click the Email address displayed in the column to open the Details page for the service account.](../images/ggl-dialogflow-srvc-account-record.png)

    The Service account details page opens.

9.  Click the **Keys** tab.

10. Click **Add Key** &gt; **Create new key**.

    ![The Add Key option is on the Keys tab for the service account.](../images/ggl-dialogflow-create-new-key.png)

11. When prompted for the key type, select **JSON**, and then click **Create**.

    The JSON file is downloaded to your computer.


**Parent Topic:**[Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ggl-dialogflow.md)

**Previous topic:**[Create a new agent in Google Dialogflow](create-new-agent-google-dialogflow.md)

**Next topic:**[Generate a Java Keystore file from the JSON private key file](generate-jks-from-json-dialogflow.md)

