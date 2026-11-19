---
title: Create a contact or consumer using Lookup and verify
description: An agent can create a contact or consumer from the Lookup and verify feature in the Contextual side panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/lookup-verify-create-contact.html
release: zurich
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Using CSM Configurable Workspace in Customer Service Management, Manage cases, Use, Customer Service Management]
---

# Create a contact or consumer using Lookup and verify

An agent can create a contact or consumer from the Lookup and verify feature in the Contextual side panel.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, workspace\_admin, admin

## About this task

Agents can use the Lookup and verify feature to search for contacts and consumers. After verifying a user's information, agents can populate that information on the interaction record.

If an agent can't find a contact or consumer, they can create a record for that user from within the Lookup and verify feature.

## Procedure

1.  Open CSM Configurable Workspace.

2.  From a saved interaction record, select one of the following icons in the Contextual side panel to access the Lookup and verify feature.

    -   Verify Contact
    -   Verify Consumer
3.  Enter user information in one of the following fields: **Verify Contact** or **Verify Consumer**.

    This information can include the first few letters of a first or last name or the first few digits of a phone or case number.

4.  If you cannot locate the contact or consumer and choose to create a record, select **Create Contact** or **Create Consumer**.

    The system displays the Create Contact or Create Consumer form in the Contextual side panel.

    If the **Account** field on the Interaction record is populated when you select **Create Contact**, the **Account** field on the Create contact form is populated with the same information.

5.  Add information to the fields on the form and select **Create**.

    The system performs the following actions:

    -   Saves the contact or consumer record.
    -   Creates and displays the contact or consumer card.
    -   Adds the information to the interaction record.

**Related topics**  


[Lookup and verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/lookup-and-verify-overview.md)

[Look up and verify a contact or consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/lookup-verify-contact-consumer.md)

