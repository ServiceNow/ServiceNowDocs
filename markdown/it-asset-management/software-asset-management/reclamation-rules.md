---
title: Reclamation rules
description: Reclamation rules define the minimum amount of time for which a subscription must be used. If the subscription doesn't have any activity within a specified time limit, it's added to the list of reclamation candidates.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 7
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Reclamation rules

Reclamation rules define the minimum amount of time for which a subscription must be used. If the subscription doesn't have any activity within a specified time limit, it's added to the list of reclamation candidates.

For each direct integration, the user activity is defined differently. Only one of the listed activities is required to occur within the specified time limit, not all of them.

<table id="table_zbp_nxp_zhb"><thead><tr><th>

Direct integration

</th><th>

Activity

</th></tr></thead><tbody><tr><td>

[Adobe Cloud](../concept/adobe-cloud-integration.md)

</td><td>

Any user activity

</td></tr><tr><td>

[Aha!](../concept/integrate-with-aha.md#)

</td><td>

User login**Note:** The analysis period is 60 days.

</td></tr><tr><td>

[Asana](../concept/integrate-with-asana.md#)

</td><td>

-   Tasks created
-   Tasks completed
-   Subtasks created
-   Subtasks completed
-   Assigning tasks or subtasks
-   Moving tasks or subtasks between projects
-   Comments added to tasks or subtasks
-   Story created

</td></tr><tr><td>

[Box](../concept/integrate-with-box.md#)

</td><td>

-   User login
-   Any file activity, including 60 actions such as create, edit, delete, share, upload, or download

</td></tr><tr><td>

[Calendly](../concept/integrate-with-calendly.md#)

</td><td>

Schedule an event

</td></tr><tr><td>

[Confluence Cloud](../concept/integrate-with-confluence-cloud.md#)

</td><td>

Create or update a space, page, blog post, comment, or attachment

</td></tr><tr><td>

Docusign

</td><td>

Subscription assigned date

</td></tr><tr><td>

[Dropbox](../concept/integrate-with-dropbox.md#)

</td><td>

-   User login
-   Any file activity, including 60 actions such as create, edit, delete, share, upload, or download

</td></tr><tr><td>

[Google Workspace](../concept/integrate-with-gsuite.md#)

</td><td>

-   **Google Drive and Google Docs**

Any file activity, such as create, edit, delete, upload, download, or sync

-   **Gmail**

Any email activity, such as read, create, edit, send, or delete


</td></tr><tr><td>

[GitHub](../concept/integrate-with-github.md)

</td><td>

-   Create a commit comment
-   Create a Git branch or tag
-   Delete a Git branch or tag
-   Fork a repository
-   Create or update a Wiki page
-   Any issue comment activity, such as create, edit, or delete
-   Any issue activity, such as open, close, reopen, assign, unassign, label, or unlabel
-   Any repository collaborator activity, such as editing the collaborator access permissions
-   Make a private repository public
-   Any pull request activity, such as open, close, reopen, assign, unassign, review, unlabel, and synchronize
-   Any pull request review comment activity
-   Push at least one commit to a repository branch or tag
-   Any release activity, such as publish or edit
-   Any sponsorship listing activity
-   Star a repository

</td></tr><tr><td>

[GoTo](../concept/integrate-with-goto.md#)

</td><td>

-   **GoToMeeting**

Host a meeting

-   **GoToWebinar**

Host a webinar or meeting

-   **GoToConnect**

Make a call using a GoToConnect line


</td></tr><tr><td>

[Jira Software](../concept/integrate-with-jira.md#)

</td><td>

-   Create an issue
-   Comment on an issue
-   Update a comment on an issue
-   Activities in the following categories:
    -   Auditing
    -   Project changes
    -   Permission changes
    -   Workflow changes
    -   Notification changes
    -   Custom field changes
    -   Advanced Roadmaps changes

</td></tr><tr><td>

[Looker](../concept/integrate-with-looker.md#)

</td><td>

User's last login

</td></tr><tr><td>

[Microsoft 365](../concept/integrate-with-microsoft.md)

</td><td>

Any user activity

</td></tr><tr><td>

[Microsoft Dynamics 365 and Power Apps](../concept/integrating-with-microsoft365.md#)

</td><td>

Create or update the following records in Dynamics 365:-   Common entities
    -   Account
    -   Contact
    -   Goal
    -   Product
    -   User
    -   Phone Call
    -   Task
    -   Letter
    -   Email
    -   Appointment
    -   Fax
    -   Custom Activities
-   Sale related entities
    -   Competitor
    -   Opportunity
    -   Invoice
    -   Order
    -   Quote
    -   Account
    -   msdyn\_relationshipinsightsunifiedconfig
    -   msdyn\_relationshipanalyticsmetadata
    -   Lead
-   Customer Service entities
    -   Case
    -   Contract
    -   Queue
    -   Service entity activity
    -   Incident

</td></tr><tr><td>

[Miro](../concept/integrate-with-miro-enterprise.md#)

</td><td>

Access or update a board

</td></tr><tr><td>

[monday.com](../concept/integrate-with-monday.md#)

</td><td>

-   Any board activity, such as create, add or remove a note, add or remove a user, and delete
-   Any item activity, such as add, edit, duplicate, and delete
-   User's last login

</td></tr><tr><td>

[PagerDuty](../concept/integrate-with-pagerduty.md#)

</td><td>

Be on an on-call schedule

</td></tr><tr><td>

[Rally](../concept/integrate-with-rally.md#)

</td><td>

-   User's last login
-   Last activity time

</td></tr><tr><td>

[Roadmunk](../concept/integrate-with-roadmunk.md#)

</td><td>

-   User login
-   Add comments to ideas or feedback
-   Create or update feedback
-   Archive or restore roadmaps

</td></tr><tr><td>

-   [Salesforce CRM](../concept/integrate-with-salesforce-crm.md#)
-   [Salesforce Marketing Cloud](../concept/integrate-with-salesforce-marketing-cloud.md)

</td><td>

Last activity

</td></tr><tr><td>

[SAP Ariba](../concept/integrate-with-ariba.md#)

</td><td>

User's last login

</td></tr><tr><td>

[SAP SuccessFactors](../concept/integrate-with-successfactors.md#)

</td><td>

User login

</td></tr><tr><td>

[Slack Enterprise](../concept/integrate-with-slack.md#)

</td><td>

User login

</td></tr><tr><td>

[SmartRecruiters](../concept/integrate-with-smartrecruiters.md#)

</td><td>

Any user activity, such as create a job or a job ad.

</td></tr><tr><td>

[Smartsheet](../concept/integrate-with-smartsheet.md#)

</td><td>

User's last activityFor the list of activities, see [Event Reporting Reference](https://smartsheet-platform.github.io/event-reporting-docs/).

</td></tr><tr><td>

[SurveyMonkey](../concept/integrate-with-surveymonkey.md#)

</td><td>

-   User login or logout
-   Update a group name
-   Add or delete a member
-   Update the group member type
-   Create or resend an invite
-   Create or update a permission
-   Create or update a shared view
-   Create or download an export
-   Update or delete a respondent
-   Create or delete grant information
-   Any survey information activity, such as create, delete, copy, update, and transfer
-   Any collector information activity, such as create, delete, and update

</td></tr><tr><td>

[Tableau Cloud](../concept/integrate-with-tableau-cloud.md#)

</td><td>

User login

</td></tr><tr><td>

[Trello](../concept/integrate-with-trello.md#)

</td><td>

User login**Note:** The analysis period is 60 days.

</td></tr><tr><td>

[Webex](../concept/integrate-with-webex-apps.md#)

</td><td>

-   **Webex Training**

Host a training

-   **Webex Events**

Host an event

-   **Webex Support Session**

Host a support session

-   **Webex Meetings**

Host a meeting

-   **Webex Teams**
    -   Send or update messages
    -   Upload a file
    -   Create or update team space memberships

</td></tr><tr><td>

[Workfront](../concept/integrate-with-workfront.md#)

</td><td>

-   Create or update projects
-   Create or update tasks
-   Create or update issues
-   Create or update portfolios
-   Create or update programs
-   Create or update reports
-   Create or update filters
-   Create or update documents
-   Create or update templates
-   Create or update expenses

</td></tr><tr><td>

Workplace from Facebook

</td><td>

-   Create, update, or view a post in a Workplace group.
-   Comment on a post in a Workplace group.
-   Send messages in the Workplace.
-   Create or update a Workplace Knowledge Library category.
-   Comment on a Workplace Knowledge Library category.
-   Create a public event in the Workplace community.

</td></tr><tr><td>

[Zendesk](../concept/integrate-with-zendesk.md#)

</td><td>

User login

</td></tr><tr><td>

[Zoom](../concept/integrate-with-zoom.md#)

</td><td>

-   Host a meeting
-   Host a webinar
-   Last activity

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Integrate with SaaS applications](../concept/create-integration-profile.md)

