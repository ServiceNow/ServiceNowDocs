---
title: Email interaction sections
description: Use the sections on the email interaction page to view and update contact, interaction, and activity details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/email-interaction-page.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 7
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction for CSM reference, Reference, Customer Service Management]
---

# Email interaction sections

Use the sections on the email interaction page to view and update contact, interaction, and activity details.

|Field|Description|
|-----|-----------|
|Name|Name of the customer contact.|
|Mobile phone|Mobile phone number of the customer contact.|
|Business phone|Business phone number of the customer contact.|
|Email|Email address of the customer contact.|
|Street|Name of the street.|
|City|Name of the city.|
|State/Province|Name of the state or province.|
|Account|Account with which the customer contact is associated.|

<table id="table_x14_hpm_q2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lookup by name, phone, or email

</td><td>

Component for looking up a contact by name, phone number, or email address: -   Search for a contact by name, phone number, or email address. Matching results appear in record cards as characters are entered in the search box.
-   Select a contact by selecting the matching record card. The record card replaces the lookup component.

You can also create a record to add a guest user as a contact. For more information, see [Create a customer contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-a-customer-contact_EaaI.md).

</td></tr></tbody>
</table><table id="table_v4m_3f1_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically created interaction number.

</td></tr><tr><td>

Type

</td><td>

Type of customer interaction, which is **Email**.

</td></tr><tr><td>

Account

</td><td>

Name of the customer contact's company. This field is filled in automatically if the information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

Name of the customer contact.

</td></tr><tr><td>

Consumer

</td><td>

Name of the consumer.

</td></tr><tr><td>

Guest Email

</td><td>

Email address of the guest user.

</td></tr><tr><td>

Verified

</td><td>

Option to mark the record as verified or validated.

</td></tr><tr><td>

State

</td><td>

Current state of the interaction. For more information, see [Interaction states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-states.md).

</td></tr><tr><td>

Assigned to

</td><td>

Name of the assigned user.

</td></tr><tr><td>

Consumer Profile

</td><td>

Information about the consumer.

</td></tr><tr><td>

Requester Organization

</td><td>

Organization requesting the omnichannel interactions.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the customer issue.

</td></tr><tr><td>

Work notes

</td><td>

Information about the interaction and the work being done to resolve the customer issue.

</td></tr></tbody>
</table><table id="table_sft_2z5_zdc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work notes

</td><td>

Internal notes documented for the agent's reference. These notes are visible only to agents and not to customer. When a work note is created, it appears in the Activity stream. For more information on work notes, see [Compose a work note for internal use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/composing-email-work-note.md).

</td></tr><tr><td>

Email

</td><td>

Compose and send emails without leaving the record. For more information, see [Compose an email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/composing-email-work-note.md).**Note:** The first email response that the agent sends is used to calculate the first response time duration, which is then populated in the **First response wait time** field.

</td></tr><tr><td>

Filters

</td><td>

Filters for emails, work notes, and field changes on the interaction.

</td></tr><tr><td>

Activity

</td><td>

View of email conversations between the agent and the customer. For more information, see [Using the activity stream in an email interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-activity-stream-in-an-email-interaction.md).

</td></tr><tr><td>

Summarize this interaction

</td><td>

Displays the AI-generated summary of the email interaction. Agents can refresh the summary, copy it, provide feedback, or save it to the interaction record. **Note:** AI-generated summaries may be inaccurate. Review the summary before using it. Check your entitlements to determine whether you have access to this feature.

</td></tr></tbody>
</table><table id="table_lhx_qz5_zdc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachments

</td><td>

Displays files and documents associated with the current record or interaction.

</td></tr><tr><td>

Recommended Actions

</td><td>

Displays the most relevant next steps based on the current context. For more information, see [Using the Recommended Actions application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-using-recommended-actions.md).

</td></tr><tr><td>

Consumer Verify

</td><td>

Confirms the identity or details of the consumer involved in the interaction. For more information, see [Lookup and verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/lookup-and-verify-overview.md).

</td></tr><tr><td>

Contact Verify

</td><td>

Confirms the identity or details of the contact involved in the interaction. For more information, see [Lookup and verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/lookup-and-verify-overview.md).

</td></tr><tr><td>

Response Template

</td><td>

Displays the response template required to respond to the customer. For more information, see [Use a response template to compose an email or a work note](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/composing-email-work-note.md).

</td></tr><tr><td>

Related Lists

</td><td>

Displays associated items such as emails, tasks, knowledge articles, and open cases linked to the current interaction.-   Related Email Interactions: Lists the email interactions linked to the current interaction.
-   Emails: Displays all the emails associated with the interaction.
-   Draft Emails: Find emails that are currently being drafted and not yet sent.
-   Related Tasks: Lists all cases created out of an interaction.
-   Related Knowledge Articles: Displays relevant knowledge articles that can provide further information related to the interaction.
-   Open Cases: Shows any open cases that are related to the consumer or contact.

</td></tr><tr><td>

Customer History

</td><td>

Displays customer, consumer, or account history information, depending on the customer information provided on the interaction record. This tab includes a search field, filter, and date range selector that agents can use to find specific information in the history. For more information on the customer history, see [Customer History component features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-history-component-features.md).

</td></tr></tbody>
</table><table id="table_overview_zdc"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Summarize

</td><td>

Generates an AI summary of the email interaction using ServiceNow Otto. The summary appears in the Interaction Summary card and may include Issue, Key Actions Taken, and Next Steps depending on the email content.**Note:** AI-generated summaries may be inaccurate. Review the summary before using it. Check your entitlements to determine whether you have access to this feature. For more information, see [AI summarization of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-ai-summarization-email-interactions.md) and [Summarize an email interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/summarize-email-interaction-eaai.md)

</td></tr><tr><td>

View less or View more

</td><td>

Collapses or expands the AI summary card.

</td></tr><tr><td>

Copy icon

</td><td>

Copies the summary content to the clipboard.

</td></tr><tr><td>

Helpful or Not helpful icons

</td><td>

Submits feedback on the quality of the AI-generated summary.

</td></tr><tr><td>

Refresh icon

</td><td>

Regenerates the summary when email interaction data has changed since the original summary was created.

</td></tr><tr><td>

Information icon

</td><td>

Displays the AI disclaimer: `AI summarized this using the record details. Check it for accuracy.`

</td></tr></tbody>
</table><table id="table_kqr_qbv_zdc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Case

</td><td>

Creates a case from the interaction.

</td></tr><tr><td>

Close

</td><td>

Closes the email interaction.

</td></tr><tr><td>

Save

</td><td>

Saves the updates made in the email interaction.

</td></tr><tr><td>

Associate Record

</td><td>

Associates existing cases with the current interaction.

</td></tr><tr><td>

Assign to me

</td><td>

Assigns the interaction to the current agent.**Note:** Assign to me is visible only in interactions in the New state and when the Assigned to field is empty.

</td></tr><tr><td>

Summarize

</td><td>

Generates an AI summary of the email interaction on demand. Check your entitlements to determine whether you have access to this feature. For more information, see [AI summarization of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-ai-summarization-email-interactions.md).

</td></tr></tbody>
</table>**Related topics**  


[Using email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)

[AI summarization of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-ai-summarization-email-interactions.md)

