---
title: Managing credit card service requests
description: By using the credit card service case and associated tasks, you can manage credit card service requests that you receive from your customers for your financial institution.
locale: en-US
release: xanadu
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Financial Services Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Managing credit card service requests

By using the credit card service case and associated tasks, you can manage credit card service requests that you receive from your customers for your financial institution.

## How to initiate credit card service requests

-   Contributors, branch workers and call center agents can submit credit card service requests on behalf of their customers from interaction records and the service catalog.
-   Customers can create requests from the Consumer Service Portal by selecting catalog items and filling out and submitting forms.

    **Note:** To enable your customers to use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).


## Assignment and resolution for credit card service cases

After requests are submitted, credit card request flows automatically create credit card service cases and tasks.

A credit card service case is used to track the overall credit card request and triggers all tasks for the request.

Each request type has a dedicated flow that triggers tasks from the parent credit card service case. The tasks that are created for a case depend on the type of credit card request type and are of the following types:

-   Credit card task – Assigned to credit card agents and used for follow-up tasks such as evaluating product eligibility and setting up a new credit card account.
-   Credit assessment task – Assigned to credit assessment agents and used for follow-up tasks that include retrieving credit assessments and evaluating risks.
-   Document service task – Assigned to document service agents and used for follow-up tasks such as document verification and preparation.

To resolve cases, agents perform activities such as gathering documents, performing credit assessments, and changing credit limits for the tasks assigned to them.

Both the case and its tasks are assigned to the assignment groups or agents by using assignment rules. For more information on assignment groups that are installed with the application, see [Configure groups](../../fso-common/task/configure-groups-fso.md).

