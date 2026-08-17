---
title: Configure Email response generation skill in ServiceNow Otto for Accounts Payable Operations \(APO\)
description: Configure the email response generation skill in ServiceNow Otto for Accounts Payable Operations \(APO\) so that accounts payable \(AP\) fulfillers can use generative AI skills in Source-to-Pay Workspace to draft professional responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/config-email-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, generative AI, Gen AI, Email response generation]
breadcrumb: [Configure ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Email response generation skill in ServiceNow Otto for Accounts Payable Operations \(APO\)

Configure the email response generation skill in ServiceNow Otto for Accounts Payable Operations \(APO\) so that accounts payable \(AP\) fulfillers can use generative AI skills in Source-to-Pay Workspace to draft professional responses.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** and select the **AI Skills** tab in the AI Admin Hub console.

2.  In the **Finance and Supply Chain** workflow group, select **Accounts Payable Operations** to view the skills for the APO features.

    1.  Select **Email response for invoice case** if you want to activate the skill for invoice case.

    2.  Select **Email response for invoice task** if you want to activate the skill for invoice task.

    For more information on email generation, see [Generate email response for invoice case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/generate-email-invoice-case-apo.md) and [Generate email response for invoice task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/generate-email-invoice-task-apo.md).

3.  Select **Activate skill**.

    A guided setup leads you through the configuration of the input, availability, access, display, review, and activation of the customized skill. If you complete the entire walk-through, the skill is activated.

4.  Select **Save and continue** to go to the next step.

5.  Configure where to display the email response for invoice case or task.

    1.  Select **In-product**.

        **In-product**: When selected, the Now Assist skills are displayed on the forms and workspaces.

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

6.  Review and activate the skill.

    For more information on drafting email responses in an invoice case or a task, see [Composing emails with predefined content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/email-composer-apm-workspace.md).


## Result

The Email generation for invoice case is activated. You can now select \[Omitted image "servicenow-otto-icon.png"\] Alt text: in the Email tab of an invoice case or a task to draft professional responses.

