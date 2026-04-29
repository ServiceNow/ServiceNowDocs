---
title: Set up Workplace from Facebook spoke
description: Integrate the ServiceNow instance and your Workplace from Facebook account using the Workplace from Facebook credentials to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workplace from Facebook Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Workplace from Facebook spoke

Integrate the ServiceNow instance and your Workplace from Facebook account using the Workplace from Facebook credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Workplace from Facebook spoke
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Workplace from Facebook** &gt; **Install on your Workplace**.

2.  Click **Install on your Workplace**.

    You will redirected to the [Workplace sign-up/sign-in](https://work.workplace.com/) page.

3.  Log in to your Workplace from Facebook account using your credentials.

    Add ServiceNow Spoke to Workplace pop-up window is displayed.

4.  Click **Add to Workplace**.

    ![Add to ServiceNow spoke to Workplace](../image/fb-add-to-workplace.png)

    The ServiceNow spoke is added to Workplace account and a confirmation message is displayed.

    ![ServiceNow spoke added to Workplace](../image/fb-confirmation.png)

5.  Click **Done**.

    You will be redirected back to your ServiceNow instance and the relevant fields are updated.

6.  If you want to create multiple connection records, perform these steps:

    1.  Navigate to **Process Automation** &gt; **Flow Designer**.

    2.  Click the **Connections** tab.

    3.  Locate the **FB\_Workplace\_Alias** connection alias and click **View Details**.

    4.  Click **Add Connection**.

    5.  Provide a name to identify the new connection record for **Connection Name**.

    6.  Click **Create Connection**.

    7.  Navigate to **All** &gt; **Workplace from Facebook** &gt; **Credentials**.

    8.  Open the credential record that is associated with the connection record you had created.

    9.  Click **Install on your Workplace**.

        You will redirected to the [Workplace sign-up/sign-in](https://work.workplace.com/) page.

    10. Log in to your Workplace from Facebook account using your credentials.

        Add ServiceNow Spoke to Workplace pop-up window is displayed.

    11. Click **Add to Workplace**.

        The ServiceNow spoke is added to Workplace account and a confirmation message is displayed.

    12. Click **Done**.

        You will be redirected back to your ServiceNow instance and the relevant fields are updated.


## Result

The Workplace from Facebook account is integrated with your ServiceNow instance.

