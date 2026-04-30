---
title: Virtual Agent conversations for Vaccine Administration Management
description: Virtual Agent conversations enable users to get help with the vaccination process.
locale: en-US
release: yokohama
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Virtual Agent conversations for Vaccine Administration Management

Virtual Agent conversations enable users to get help with the vaccination process.

If the Virtual Agent plugin \(com.glide.cs.chatbot\) is installed, the Vaccine Administration Management provides Virtual Agent conversation topics. A conversation topic defines the dialog between the Virtual Agent \(chatbot\) and the user to accomplish a goal.

<table id="table_ulq_1hd_l4b"><thead><tr><th>

Topic

</th><th>

Description

</th><th>

Default status

</th></tr></thead><tbody><tr><td>

Book Appointment

</td><td>

Enables users to book vaccination appointments through the chatbot.

 The questions asked in this topic are the default questions that a user must answer when booking an appointment in the self-service portal.

**Note:** This topic is a placeholder conversation topic. You can change the questions according to your requirements.

</td><td>

Inactive

</td></tr><tr><td>

My Vaccination Phase Eligibility

</td><td>

Informs users about vaccination eligibility and enables users to book an appointment if the user is eligible.

**Note:** This topic is a placeholder conversation topic. You can change the questions according to your requirements.

</td><td>

Active

</td></tr><tr><td>

COVID-19 Vaccine resources

</td><td>

Shows targeted Knowledge articles to the user.

**Note:** To use this topic, you must activate the ServiceNow® Service Management Topic Blocks plugin \(com.glideapp.cs.sm\_topic\_blocks\).

 The articles shown in this topic are set by a keyword. By default, the topic shows all articles that contain the keyword “vaccine.” To change the keyword, navigate to this topic in the ServiceNow® Virtual Agent Designer. In the topic, click the **Contextual Search** block. In the Topic Block Properties panel, set the value of the **query** field to the new keyword.

</td><td>

Inactive

</td></tr><tr><td>

COVID-19

</td><td>

Enables users to report vaccination status and COVID-19 test results using topic blocks.

-   **Report vaccination status**: Enables users to report the vaccination status.

**Note:** This topic is a placeholder conversation topic. You can change the questions according to your requirements.

-   **Report COVID-19 test results**: Enables users to report COVID-19 test results.

**Note:** This topic is a placeholder conversation topic. You can change the questions according to your requirements.


 Non-logged in users who are non-registered users must provide a first name, last name, and email address before they self-report their vaccination status or COVID-19 test results.

 When users report their vaccination status or COVID-19 test results, email notifications are automatically sent to the user's email ID.

</td><td>

Active

</td></tr></tbody>
</table>To activate, deactivate, or edit conversation topics, navigate to **Collaboration** &gt; **Virtual Agent** &gt; **Designer**. In the Topics page, select the **Vaccine Management** category. Click a topic that you want to update. Use the **Active** toggle button to activate or deactivate a topic.

**Parent Topic:**[Configuring Vaccine Administration Management](vaccine-mgmt-config.md)

