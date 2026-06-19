---
title: Create a service account and private key for the Google Dialogflow project
description: To use Google Dialogflow with Virtual Agent Bot Interconnect, the second step is to create a service account and private key for the new agent in Google Dialogflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/create-srvc-acct-key-dialogflow.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a service account and private key for the Google Dialogflow project

To use Google Dialogflow with Virtual Agent Bot Interconnect, the second step is to create a service account and private key for the new agent in Google Dialogflow.

## Before you begin

Role required: admin

## Procedure

1.  On the project dashboard page, click **Go to project settings**.

    \[Omitted image "ggl-dialogflow-go-project-settings.png"\] Alt text: On the Google Cloud Home dashboard, Go to project settings displays on the Project info card.

2.  On the IAM &amp; Admin page, click **Service Accounts**.

3.  Click **+ Create Service Account**.

    \[Omitted image "ggl-dialogflow-create-srvc-account.png"\] Alt text: When you select the Service Accounts option in the side menu, the Create Service Account option appears in the header bar.

4.  Provide a name, and then click **Create and Continue**.

5.  Under Select a role, select **Dialogflow** &gt; **Dialogflow API Client**.

6.  Click **Continue**.

    \[Omitted image "ggl-dialogflow-assign-role.png"\] Alt text: Assign the Dialogflow API Client role on the service account details screen, then click Continue to go to the next step.

7.  Click **Done**.

8.  Click the link for the record in the **Email** column.

    \[Omitted image "ggl-dialogflow-srvc-account-record.png"\] Alt text: The Service accounts screen displays the email, name, and description. Click the Email address displayed in the column to open the Details page for the service account.

    The Service account details page opens.

9.  Click the **Keys** tab.

10. Click **Add Key** &gt; **Create new key**.

    \[Omitted image "ggl-dialogflow-create-new-key.png"\] Alt text: The Add Key option is on the Keys tab for the service account.

11. When prompted for the key type, select **JSON**, and then click **Create**.

    The JSON file is downloaded to your computer.


**Parent Topic:**[Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/using-va-api-ggl-dialogflow.md)

**Previous topic:**[Create a new agent in Google Dialogflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-new-agent-google-dialogflow.md)

**Next topic:**[Generate a Java Keystore file from the JSON private key file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/generate-jks-from-json-dialogflow.md)

