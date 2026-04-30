---
title: Tutorial part 8: Generate a playbook with Now Assist
description: Playbooks provide a streamlined and automated process for specific activities. The playbook automates sending feedback requests to event attendees, ensuring efficient and consistent collection. This eliminates manual effort and enables timely communication, allowing for easy gathering of valuable insights to improve future events and the attendee experience.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 8: Generate a playbook with Now Assist

Playbooks provide a streamlined and automated process for specific activities. The playbook automates sending feedback requests to event attendees, ensuring efficient and consistent collection. This eliminates manual effort and enables timely communication, allowing for easy gathering of valuable insights to improve future events and the attendee experience.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  From the We Volunteer app dashboard, select **Create** &gt; **File**.

2.  Enter **Global** in the Application field.

3.  Under the Automation category, select **Playbook**.

4.  Select **Continue**.

5.  On the Build with Now Assist tab, enter the following information for the playbook:

    -   Playbook name: `Collect feedback from attendees`
    -   Now Assist directions: `I want to create a playbook on the Event (x_snc_wevolunteer_event) table, which has following steps: Stage 1: Instructions - This stage involves providing instructions to volunteer admins that validate the attendee’s information for the event and send emails to them to collect feedback for the event. Stage 2: List of attendees - This stage involves looking up attendees table (x_snc_wevolunteer_attendees) records for triggered event. Stage 3: Collect feedback by sending email. The email could include links to the record producer by which attendees can provide their feedback.`
6.  Select **Generate playbook preview**.

7.  Select **Save and edit playbook**.

    ![Playbook preview](../image/sn-studio-tutorial-playbook-preview.png)


**Parent Topic:**[ServiceNow Studio tutorial](../concept/lab-sns-lab-guide.md)

