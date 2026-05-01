---
title: Reclamation rules for SaaS and SSO applications
description: Reclaim unused SaaS and Single sign-on \(SSO\) subscriptions to reduce your total software costs.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 12
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Reclamation rules for SaaS and SSO applications

Reclaim unused SaaS and Single sign-on \(SSO\) subscriptions to reduce your total software costs.

Reclamation rules define the minimum amount of time for which a subscription must be used. If the subscription doesn't have any activity within a specified time limit, it's added to the list of reclamation candidates.

For each direct integration, the user activity is defined differently. Only one of the listed activities is required to occur within the specified time limit, not all of them.

**Warning:** Make sure that users don't lose access to their files when their account is reclaimed. Users can't stop their account from being reclaimed unless the **Notify user** check box is selected on the reclamation rule.

Automatic reclamation is unavailable for some SaaS applications. For these applications, update or remove licenses manually from the application's admin portal.

<table id="table_reclamation-saas-sso"><thead><tr><th>

Application

</th><th>

Activity considered for reclamation

</th><th class="filter">

Is reclamation automated?

</th><th>

What happens after auto-reclamation?

</th></tr></thead><tbody><tr><td>

[Adobe Cloud](../concept/adobe-cloud-integration.md)

</td><td>

Any user activity

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[Adobe Workfront](../concept/integrate-with-workfront.md#)

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

</td><td>

Yes

</td><td>

Removes the user's access to the Workfront application. The user is no longer allowed to sign in.

</td></tr><tr><td>

[Aha!](../concept/integrate-with-aha.md#)

</td><td>

User login**Note:** The analysis period is 60 days.

</td><td>

Yes

</td><td>

Deactivates the account. The user can’t log in to the Aha! portal.

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

</td><td>

Yes

</td><td>

Deletes the user account. The user can no longer access Asana projects or workspace. Content created by the user remains accessible to other users and the admin can reassign tasks from the Asana dashboard.

</td></tr><tr><td>

[Box](../concept/integrate-with-box.md#)

</td><td>

-   User login
-   Any file activity, including 60 actions such as create, edit, delete, share, upload, or download

</td><td>

Yes

</td><td>

Deletes the user account. All files are moved into a folder in the Box admin account that authenticated the integration.

</td></tr><tr><td>

[Calendly](../concept/integrate-with-calendly.md#)

</td><td>

Schedule an event

</td><td>

Yes

</td><td>

Removes the account from your organization.

</td></tr><tr><td>

[Confluence Cloud](../concept/integrate-with-confluence-cloud.md#)

</td><td>

Create or update a space, page, blog post, comment, or attachment

</td><td>

Yes

</td><td>

Removes the user from all associated Confluence groups. The user can no longer access the Confluence site, but the content created by the user remains accessible to other users.

</td></tr><tr><td>

[Docusign Account level](../concept/integrate-with-docusign-account.md#)

</td><td>

Subscription assigned date

</td><td>

Yes

</td><td>

Deletes the account. Docusign admin can access user's files via the Docusign admin portal.

</td></tr><tr><td>

[Docusign Organization level](../concept/integrate-with-docusign-org.md#)

</td><td>

Subscription assigned date

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[Dropbox](../concept/integrate-with-dropbox.md#)

</td><td>

-   User login
-   Any file activity, including 60 actions such as create, edit, delete, share, upload, or download

</td><td>

Yes

</td><td>

Deletes the account. All files are moved into a folder \(named after deleted user's email\) in the Dropbox admin account that authenticated the integration.

</td></tr><tr><td>

[Google Workspace](../concept/integrate-with-gsuite.md#)

</td><td>

-   **Google Drive and Google Docs**

Any file activity, such as create, edit, delete, upload, download, or synchronize

-   **Gmail**

Any email activity, such as read, create, edit, send, or delete


</td><td>

Yes

</td><td>

Deletes the account. All files are moved from Google Drive into a folder \(named after deleted user's email\) in the Google Workspace admin account. All email messages are deleted when the account is reclaimed. To transfer email messages, use the Google data migration service before reclaiming the account.

</td></tr><tr><td>

[GitHub](../concept/integrate-with-github.md)

</td><td>

-   Create a commit comment
-   Create a Git branch or tag
-   Delete a Git branch or tag
-   Fork a repository
-   Create or update a wiki page
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

</td><td>

Yes

</td><td>

-   **GitHub Enterprise Server**

Suspends the account. All issues, comments, repositories, gists, and other data created by the user are preserved.

-   **GitHub Enterprise Cloud**

Removes the account from all enterprise organizations. Restoring membership within three months of reclamation restores the user access to private forks of your organization.


</td></tr><tr><td>

[GoTo](../concept/integrate-with-goto.md#)

</td><td>

-   **GoToMeeting**

Host a meeting

-   **GoToWebinar**

Host a webinar or meeting

-   **GoToConnect**

Call using a GoToConnect line


</td><td>

Yes

</td><td>

Reclaiming a product license from a GoTo user account removes the user's access to that product. Without a license, users can't sign in to the product. If all product licenses are reclaimed, the account is automatically suspended, preventing sign-in to any products.

</td></tr><tr><td>

[Jira Software](../concept/integrate-with-jira.md)

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

</td><td>

Yes

</td><td>

Removes the user from all associated Jira groups. The user can no longer access the Jira site, but the content created by the user remains accessible to other users.

</td></tr><tr><td>

[Looker](../concept/integrate-with-looker.md#)

</td><td>

User's last login

</td><td>

Yes

</td><td>

Removes the user's access to Looker, preventing sign-in. Usage history and personal content are retained.

</td></tr><tr><td>

[Microsoft 365](../concept/integrate-with-microsoft.md)

</td><td>

Any user activity

</td><td>

Yes

</td><td>

Removes the user's access to the application, associated plans, and services. If a user has access to an application through a group membership, reclaiming the subscription removes the user from the group and revokes access to the subscription and its associated plans.

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
-   Sale-related entities
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

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[Miro](../concept/integrate-with-miro-enterprise.md#)

</td><td>

Access or update a board

</td><td>

Yes

</td><td>

Removes user's access to Miro, preventing sign-in.

</td></tr><tr><td>

[monday.com](../concept/integrate-with-monday.md#)

</td><td>

-   Any board activity, such as create, add or remove a note, add or remove a user, and delete
-   Any item activity, such as add, edit, duplicate, and delete
-   User's last login

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[PagerDuty](../concept/integrate-with-pagerduty.md#)

</td><td>

Be on an on-call schedule

</td><td>

Yes

</td><td>

Deletes the account.

</td></tr><tr><td>

[Rally](../concept/integrate-with-rally.md#)

</td><td>

-   User's last login
-   Last activity time

</td><td>

Yes

</td><td>

Removes the user's access to Rally, preventing sign-in.

</td></tr><tr><td>

[Roadmunk](../concept/integrate-with-roadmunk.md#)

</td><td>

-   User login
-   Add comments to ideas or feedback
-   Create or update feedback
-   Archive or restore roadmaps

</td><td>

Yes

</td><td>

NA

</td></tr><tr><td>

-   [Salesforce CRM](../concept/integrate-with-salesforce-crm.md#)
-   [Salesforce Marketing Cloud](../concept/integrate-with-salesforce-marketing-cloud.md)

</td><td>

Last activity

</td><td>

Yes

</td><td>

Deactivates the user.

</td></tr><tr><td>

[SAP Ariba](../concept/integrate-with-ariba.md#)

</td><td>

User's last login

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[SAP SuccessFactors](../concept/integrate-with-successfactors.md#)

</td><td>

User login

</td><td>

Yes

</td><td>

Deactivates the account.

</td></tr><tr><td>

[SAP S/4HANA](../concept/integrate-with-hana.md#)

</td><td>

 

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[Slack Enterprise](../concept/integrate-with-slack.md#)

</td><td>

User login

</td><td>

Yes

</td><td>

Deactivates the user. Messages and files are saved, but the user is removed from all channels and signed out of workspaces, and can't sign back in.

</td></tr><tr><td>

[SmartRecruiters](../concept/integrate-with-smartrecruiters.md#)

</td><td>

Any user activity, such as create a job or a job ad.

</td><td>

Yes

</td><td>

Removes access to the application. For example, you might want to reclaim the accounts of users who aren't actively using the application or who have quit the organization.

</td></tr><tr><td>

[Smartsheet](../concept/integrate-with-smartsheet.md#)

</td><td>

User's last activityFor the list of activities, see [Event Reporting Reference](https://smartsheet-platform.github.io/event-reporting-docs/).

</td><td>

Yes

</td><td>

Removes the user from your organization account, downgrading them to a free collaborator with read-only access to the reports, sheets, sights, workspaces, and shared templates that haven't been transferred to other users.

</td></tr><tr><td>

[Single Sign-on \(SSO\) subscriptions](../concept/saas-sso-integration.md)

</td><td>

Unused subscriptions or subscriptions with limited to no activity.

</td><td>

Yes

</td><td>

Depends on the specific application's integration and configuration.

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

</td><td>

No

</td><td>

NA

</td></tr><tr><td>

[Tableau Cloud](../concept/integrate-with-tableau-cloud.md#)

</td><td>

User login

</td><td>

Yes

</td><td>

Removes the user from a site only if they don't own content. If they own content, their site role changes to Unlicensed and they are removed from groups, but not completely from the site.

</td></tr><tr><td>

[Trello](../concept/integrate-with-trello.md#)

</td><td>

User login**Note:** The analysis period is 60 days.

</td><td>

Yes

</td><td>

Removes user's access to enterprise content or features. You can log in but can't access previously accessed boards and cards.

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

</td><td>

Yes

</td><td>

Removes the user's access to the specific product. The user can still access other Cisco Webex products and free licenses.

</td></tr><tr><td>

[Workplace from Facebook](../concept/integrate-with-workplace.md#)

</td><td>

-   Create, update, or view a post in a Workplace group.
-   Comment on a post in a Workplace group.
-   Send messages in the Workplace.
-   Create or update a Workplace Knowledge Library category.
-   Comment on a Workplace Knowledge Library category.
-   Create a public event in the Workplace community.

</td><td>

Yes

</td><td>

Removes the user's access to Workplace. Account is deactivated, preventing login. Posts, comments, and messages remain available.

</td></tr><tr><td>

[Zendesk](../concept/integrate-with-zendesk.md#)

</td><td>

User login

</td><td>

Yes

</td><td>

Removes user's access to the Zendesk application, preventing sign-in.

</td></tr><tr><td>

[Zoom](../concept/integrate-with-zoom.md#)

</td><td>

-   Host a meeting
-   Host a webinar

</td><td>

Yes

</td><td>

Downgrades the account to Zoom Basic. All cloud-recorded meetings are deleted, but the locally saved recordings aren't affected.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

