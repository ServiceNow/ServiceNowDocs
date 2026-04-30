---
title: Perform a questionnaire-based post incident review
description: You may decide that a post incident review of the security incident is warranted. A post incident review describes what happened, helps to determine why the incident occurred, and identifies how it can be avoided or handled in the future.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform a questionnaire-based post incident review

You may decide that a post incident review of the security incident is warranted. A post incident review describes what happened, helps to determine why the incident occurred, and identifies how it can be avoided or handled in the future.

## Before you begin

Role required: sn\_si.admin, sn\_si.manager, sn\_si.analyst

**Note:** Any user can participate in a post incident review questionnaire, regardless of role. Roles can be assigned to a review.

## About this task

The ServiceNow Security Incident Response application can automate the collection of post incident review information from everyone involved with a security incident by using questionnaires. If you decide to use a questionnaire as part of a post incident review, a list of questions, relevant to the security incident, is sent to the user-defined list of participants. As each user completes the questionnaire, the post incident report is automatically generated. The report compiles all the information related to the security incident, as well as all responses to the post incident review.

While an initial list of questions is provided with the base system, they are customizable. You can create categories and add new questions to them, or you can change individual questions within existing categories. You can ask questions based on roles. You can define when certain questions are asked. There can be questions you ask only for your UNIX servers, for example, or only when there is criminal activity. You can define questions that are asked depending on the answer to another question or on the value in a field on the form. There can even be questions that are filled in entirely by querying the database.

After the security incident is resolved and moved to **Review** state, assessments are generated for all assigned users and users who are directly added from the **Request assessments** list.

The questionnaire can be a helpful tool for gathering information about the handling of the security incident from various sources.

During the review, you can add more users to the list or remove existing users from the list, unless they have already started filling out the questionnaire. If you add new users to the list, they receive the questions when the record is saved. The security incident cannot be closed until all questionnaires have been completed. As questionnaires are completed by each user, the post incident report is automatically generated \(and regenerated\) and displayed on the **Post Incident Review** tab.

To start a post incident review:

## Procedure

1.  [Create a security incident](../concept/si-creation.md), or open an existing one by navigating to **Security Incident** &gt; **Incidents** &gt; **Assigned to Me \(or Assigned to Team or Unassigned Incidents\)**.

2.  Click the **Post Incident Review** tab.

3.  The **Request assessments** field defaults to the individual in the **Assigned to** field.

    Click the lock icon to add other users to the review list. After the field is unlocked, options are available for adding or removing multiple users, roles, or entering user email addresses.

4.  When you have completed your entries, click the lock icon to lock the field.

    **Note:** You can also define conditions which, when met in a security incident, can cause specific users to be automatically added to the **Request assessments** field for that security incident. For example, when a security incident **Category** is changed to **Phishing**, specific individuals who have expertise in phishing threats can be added to the post incident review list. For more information, see [Create PIR assignment rules](create-pir-assignment-rules.md).

5.  Click **Update**.

    When the incident goes into the **Review** state \(or immediately, if it is already in the **Review** state\), each of the users in the review list receives an initial [email notification](https://www.servicenow.com/docs/access?context=r_AssessmentNotifications&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Reminders are sent as the due date nears. When each user accesses the questionnaire from the email link or by going to **Post Incident Review** &gt; **My Pending Reviews**, the questions shown are drawn from all categories that fit this security incident. If new users are added to the review list before the due date is reached, they are sent notifications when the security incident is saved.

    As users complete their questionnaires, the post incident report compiles the data and displays the report in the **Post Incident Review** tab. The questionnaire data is displayed in the **Findings** tab.


