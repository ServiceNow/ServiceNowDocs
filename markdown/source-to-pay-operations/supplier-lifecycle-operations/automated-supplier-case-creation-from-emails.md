---
title: Automate supplier case creation from emails
description: Emails received from supplier contacts can be automatically converted to supplier cases using the Email Intent to Action Agentic workflow.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-02-09"
reading_time_minutes: 2
breadcrumb: [Use, Now Assist for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Automate supplier case creation from emails

Emails received from supplier contacts can be automatically converted to supplier cases using the Email Intent to Action Agentic workflow.

The Email Intent to Action Agentic workflow analyzes incoming supplier emails, identifies the email intent, and executes associated actions using the Intent Identification and Intent Executor agents. For more information on the Email Intent to Action Agentic workflow, see [Email Intent to Action Agentic Workflow](https://www.servicenow.com/docs/access?context=email-agentic-workflow&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Prerequisites for automated creation of supplier cases

To use this functionality, verify that the following steps are completed:

-   Configure the \[sn\_supplier.slm\_email\] system property and edit the Value field to contain supplier email address. For more information, see [Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md).
-   Deactivate the Create Supplier case for email inbound action. For more information, see [Deactivate Create supplier case from email inbound action](deactivate-create-supplier-case-from-email-inbound-action.md).
-   Activate the Trigger Intent to Action inbound action. For more information, see [Enable intent to action workflow from inbound actions](https://www.servicenow.com/docs/access?context=enable-intent-to-action&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Automatic creation of supplier cases workflow

1.  When an email arrives in a supplier’s inbox, the sender details are verified. If the sender is not a registered supplier contact, an automated reply is sent for registration.
2.  If the sender is a registered supplier contact but is mapped to several suppliers, an automated reply is sent to request clarification.
3.  The Intent Identification Agent analyzes the inbound email and identifies its intent. Once identified, this intent is mapped to a preconfigured and customized intent within the system. For more information, see [Create and associate actions for intent](https://www.servicenow.com/docs/access?context=create-actions-for-intent&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
4.  The Intent Executor Agent creates cases based on the following criteria:

    -   If the email contains SLO related queries, a supplier case is created for each of the queries. The cases are assigned automatically to the supplier relationship manager.
    -   If the email contains vague information or queries unrelated to SLO, a universal request is created.
    -   If the email contains multiple queries, supplier cases are created to resolve SLO related queries and a single universal request is created for other queries.

**Related topics**  


[Deactivate Create supplier case from email inbound action](deactivate-create-supplier-case-from-email-inbound-action.md)

