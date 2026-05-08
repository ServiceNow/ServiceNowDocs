---
title: Email interaction sections
description: The Email interaction sections enable you to manage information within the interaction record.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction for CSM reference, Reference, Customer Service Management]
---

# Email interaction sections

The Email interaction sections enable you to manage information within the interaction record.

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

The contact lookup component enables agents to do the following:-   Look up a contact by name, phone number, or email address. As the agent types characters in the search box, matching information appears in record cards below the search box.
-   Select a contact after searching by selecting the record card. The selected record card replaces the lookup component.

You can also create a record to add a guest user as a contact. For more information, see [Create a customer contact](../task/create-a-customer-contact_EaaI.md).

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

Email ID of the guest user.

</td></tr><tr><td>

Verified

</td><td>

Option to mark the record as verified or validated.

</td></tr><tr><td>

State

</td><td>

Current state of the interaction. For more information, see Interaction states.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the assigned user.

</td></tr><tr><td>

Consumer Profile

</td><td>

Information about the consumer.

</td></tr><tr><td>

Requestor Organization

</td><td>

Organization requesting the omni-channel interactions

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

Internal notes documented for agent’s reference. These notes are visible only to agents and not to the customer. When a work note is created, it appears in the Activity stream. For more information on work notes, see [Compose a work note for internal use](../concept/composing-email-work-note.md#).

</td></tr><tr><td>

Email

</td><td>

Compose and send emails without leaving the record. For more information, see [Compose an email response](../concept/composing-email-work-note.md#).**Note:** The first email response that the agent sends is used to calculate the first response time duration, which is then populated in the **First response wait time** field.

</td></tr><tr><td>

Filters

</td><td>

Enables you to filter emails, work notes, and field changes on the interaction.

</td></tr><tr><td>

Activity

</td><td>

Enables agents to view the email conversations between the agent and customer. For more information, see [Using the activity stream in an email interaction](../concept/using-activity-stream-in-an-email-interaction.md).

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

Displays the most relevant next steps based on the current context. For more information, see [Using the Recommended Actions application](../concept/ra-csm-using-recommended-actions.md).

</td></tr><tr><td>

Consumer Verify

</td><td>

Confirms the identity or details of the consumer involved in the interaction. For more information, see [Lookup and verify](../../../administer/workspace/concept/lookup-and-verify-overview.md).

</td></tr><tr><td>

Contact Verify

</td><td>

Confirms the identity or details of the contact involved in the interaction. For more information, see [Lookup and verify](../../../administer/workspace/concept/lookup-and-verify-overview.md).

</td></tr><tr><td>

Response Template

</td><td>

Displays the response template required to respond to the customer. For more information, see [Use a response template to compose an email or a work note](../concept/composing-email-work-note.md#).

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

Displays customer, consumer, or account history information, depending on the customer information provided on the interaction record. This tab includes a search field, filter, and date range selector that agents can use to find specific information in the history. For more information on the customer history, see [Customer History component features](../concept/customer-history-component-features.md).

</td></tr></tbody>
</table><table id="table_kqr_qbv_zdc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Case

</td><td>

Enables the creation of a new case from the interaction.

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

Enables associating the existing cases with the current interaction.

</td></tr><tr><td>

Assign to me

</td><td>

Assigns the interaction to the current agent.**Note:** Assign to me is visible only in interactions in the New state and with the Assigned to field as empty.

</td></tr></tbody>
</table>**Related topics**  


[Using the email interaction page](../concept/using-email-interaction-page.md)

