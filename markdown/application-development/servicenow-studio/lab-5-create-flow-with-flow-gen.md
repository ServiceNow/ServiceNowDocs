---
title: Tutorial part 5: Create a flow with Flow Generation
description: Use Now Assist to create a flow for your app in ServiceNow Studio.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 5: Create a flow with Flow Generation

Use Now Assist to create a flow for your app in ServiceNow Studio.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to the We Volunteer app dashboard, and select **Create** &gt; **File**.

2.  Enter **Global** in the Application field.

3.  Under the Automation category, select **Flow**.

4.  Select **Continue**.

5.  On the Build with Now Assist tab, enter the following information:

    -   Flow name: Update Event State to Expired
    -   Now Assist directions: `Create a flow that runs every day at midnight and then find event(x_snc_wevolunteer_event) records for where ends(ends) field value is of yesterday. Iterate over them. move the state to "expired," and then send a notification to the organizer of the event record.`
6.  Select **Generate flow preview**.

    **Note:** If you're prompted to keep or remove formatting in pasted content, select **Remove formatting**.

    The flow is generated on the right side of your screen in a flow preview.

    ![Preview of a flow.](../image/sn-studio-tutorial-flow-preview.png)

7.  Select **Save and edit flow**.


**Parent Topic:**[ServiceNow Studio tutorial](../concept/lab-sns-lab-guide.md)

