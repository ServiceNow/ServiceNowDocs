---
title: ITSM Virtual Agent pre-built LLM topics
description: ITSM Virtual Agent includes pre-built Large Language Model \(LLM\) topic conversations designed to help your users complete the common IT-related tasks such as checking and resetting a password.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure in Virtual Agent, Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# ITSM Virtual Agent pre-built LLM topics

ITSM Virtual Agent includes pre-built Large Language Model \(LLM\) topic conversations designed to help your users complete the common IT-related tasks such as checking and resetting a password.

LLMs are used to identify and trigger the action that a user wants to perform.

ITSM Virtual Agent pre-built LLM topics are read only and have **\(Template\)** as the suffix in their name. To use them, duplicate the topic in the ITSM Virtual Agent conversation scope and rename it according to your company naming conventions.

For ITSM Virtual Agent pre-built Natural Language Understanding \(NLU\) topics, see [Using ITSM Virtual Agent pre-built topics](../../itsm-virtual-agent/concept/using-itsm-va.md).

**Note:** All demo topics will be available with the demo data.

<table id="table_an3_5t2_4bc"><tbody><tr><td>

Check Ticket and Support Status

</td><td>

Check the status of your IT tickets and support cases.

 Once the conversation is initiated, it progresses by collecting data about the ticket one question at a time.

**Note:** For HR cases, an Admin must allow Core RCA records for Read operation and Write operation.

-   sys\_scope = Now Assist in Virtual Agent
-   target\_scope = Human Resources: Core
-   target = Table: HR Case
-   status = Allowed
-   source = Script Include: ITSMTopicsHelper

See [Requested restricted caller access \(RCA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/requested-rca.md) for more information.

</td></tr><tr><td>

Show Pending Approvals

</td><td>

Check pending approvals that are needed to take action upon and pick those to be processed.

 You can either Approve or Reject your tickets by picking the list numbers provided to you by the Virtual Agent.

</td></tr><tr><td>

Check your device's health using Digital End-User Experience \(DEX\)

</td><td>

Use the Now Assist for ITSM Virtual Agent to monitor your device's performance and diagnose potential issues. See [Check device health using Now Assist for ITSM Virtual Agent](../../digital-end-user-experience/task/check-your-device-s-health-using-now-assist-for-itsm.md) for more information.**Important:** You must install DEX to perform this action. See [Install Digital End-User Experience](../../digital-end-user-experience/task/install-app-device-health.md) for more information.

</td></tr><tr><td>

\(DEMO\) Explain change risk

</td><td>

Quickly generate the explanation of the calculated risk rating for a change request by using the change request risk explanation skill in the Now Assist for IT Service Management \(ITSM\) application.

</td></tr></tbody>
</table>## Core ITSM topics

<table id="table_us4_xc3_nbc"><tbody><tr><td>

\(DEMO\) Check IT Ticket Status \(Template\)

</td><td>

Check the status of your IT ticket.

 Once the conversation is initiated, it progresses by collecting data about the ticket one question at a time.

</td></tr><tr><td>

\(Deprecated\) Escalate IT Ticket

</td><td>

Raise the urgency of your IT ticket for a faster resolution. Escalating a ticket priority requires choosing the incident and verifying the escalation.

 Users must provide a justification to escalate the incident. Virtual Agent escalates the incident to the next urgency level. For example, from low to medium, or from medium to high.

 If an incident is already at high-level urgency, Virtual Agent alerts the user to this and asks if the user would like to add a comment to help expedite resolution.

</td></tr><tr><td>

\(DEMO\) Open IT Ticket \(Template\)-LLM

</td><td>

Open a ticket leveraging machine-learning algorithms with application logic for predicting similar open tickets.

 Prevent users from opening duplicate incidents by finding similar incidents and asking if the user wants to add comments to the similar incident.

</td></tr><tr><td>

Service Disruptions

</td><td>

Access all known outage information.

 When a user asks if a particular system is down, Virtual Agent returns a list of links displaying planned or unplanned outages and any system degradations.

 Users can click the links for more detailed information about a specific outage or degradation, as well as click **Show more** when additional outages are known.

</td></tr></tbody>
</table>## Password reset topics

End users can initiate a password management conversation with Virtual Agent by entering the keywords `Reset`, `Change`, `Unlock`, or `Password`.

Users who aren’t logged in can perform the Reset Password and Unlock Account actions. Users who are logged in can perform the Change Password, Reset Password, and Unlock Password actions.

Requirements:

-   Password Reset \(com.glideapp.password\_reset\) plugin
-   Password Reset Virtual Agent Conversations \(com.snc.password\_reset.virtual\_agent\) plugin

**Note:** For the password reset process to be available in Virtual Agent, ensure that you selected the **Enabled on Virtual Agent** check box in the Password Reset process configuration page.

For more information about the password reset process, see [Password Reset for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/password-reset-for-virtual-agent.md).

<table id="table_zc2_s23_nbc"><tbody><tr><td>

\(DEMO\) Change Password \(Template\)-LLM

</td><td>

Request to change your user password.

 User must be logged in.

</td></tr><tr><td>

\(DEMO\) Reset Password \(Template\) - LLM

</td><td>

Request to reset your user password.

</td></tr><tr><td>

\(DEMO\) Unlock Account \(Template\) - LLM

</td><td>

Request to verify your locked user account.

</td></tr></tbody>
</table>The following identity verification options are supported for password reset in Virtual Agent conversations. Custom verifications aren’t supported in Virtual Agent.

-   Personal data verification: User provides specific pieces of personal data.
-   Google Authenticator verification: User enters the generated code from the Google service Authenticator mobile app.
-   SMS code verification: User enters the code received via a mobile text message.
-   Email code verification: User enters the code received via email.
-   Security question verification: User enters the configured security question answers.

For more information, see [Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md).

## Actionable notification topics

ITSM Virtual Agent includes pre-built actionable notifications used to send interactive messages to a user based on pending tasks or alerts, such as RITM and request notifications, task approval notifications, and incident notifications.

**Note:** You must activate notifications in Workflow Studio. For details, see [Set up actionable notifications for ITSM Virtual Agent](../../itsm-virtual-agent/task/setup-actionable-notifications.md).

<table id="table_x5c_n1w_bdc"><thead><tr><th>

Topic

</th><th>

Actionable notification

</th></tr></thead><tbody><tr><td>

RITM View Comment

</td><td>

Notification: Requested Item commented

 Sent to the approver of a Service Catalog request.

</td></tr><tr><td>

RITM Add Comments

</td><td>

Notification: Requested item on behalf of requester

 Sent to the end user when a Service Catalog request is opened on the end user's behalf.

</td></tr><tr><td>

View Request Details for Approver

</td><td>

-   Notification: Request approval reminder

Sent to the approver of a Service Catalog request.

-   Notification: Approval request for requests

Sent to the end user who made the change request when an approval for a change is requested.


</td></tr><tr><td>

View RITM Details For Approver

</td><td>

-   Notification: Approval request for requested items

Sent to the approver of a Service Catalog item request.

-   Notification: Requested Item approval reminder

Sent to remind the approver of a pending Service Catalog request.


</td></tr><tr><td>

View RITM Details For Requester

</td><td>

Notification: Requested item on behalf of requester

 Sent to the end user when a Service Catalog request is opened on the end user's behalf.

</td></tr></tbody>
</table><table id="table_qjn_5xv_bdc"><thead><tr><th>

Topic

</th><th>

Actionable notification

</th></tr></thead><tbody><tr><td>

\(DEMO\) Add Comment To Incident-LLM

</td><td>

Notification: Incident on behalf of callerSent to end users whenever an incident is opened on their behalf.

</td></tr><tr><td>

\(DEMO\) Close Incident-LLM

</td><td>

Notification: Incident resolvedSent to end users whenever one of their incidents is resolved by someone other than the end user.

</td></tr><tr><td>

\(DEMO\) Mark Incident Unresolved-LLM

</td><td>

Notification: Incident resolvedSent to end users whenever one of their incidents is resolved by someone other than the end user.

</td></tr><tr><td>

\(DEMO\) View And Add Comments-LLM

</td><td>

Notification: Incident commentedSent to end users whenever a comment is added to their incident by someone other than the end user.

</td></tr><tr><td>

\(DEMO\) Resolve Incident-LLM

</td><td>

-   Notification: Incident commented

Sent to end users whenever a comment is added to their incident by someone other than the end user.

-   Notification: Incident on behalf of caller

Sent to end users whenever an incident is opened on their behalf.


</td></tr></tbody>
</table><table id="table_u5k_kmb_cdc"><thead><tr><th>

Topic

</th><th>

Actionable notification

</th></tr></thead><tbody><tr><td>

Approve Sysapproval Approver

</td><td rowspan="3">

-   Notification: Other approval

Sent to the approver when a non-task record \(such as a Knowledge Base article\) needs approval.

-   Notification: Task approval

Sent to the approver about a newly created task that needs review and approval.


</td></tr><tr><td>

\(DEMO\) Reject Sysapproval Approver-LLM

</td></tr><tr><td>

Show Approval Details

</td></tr></tbody>
</table>