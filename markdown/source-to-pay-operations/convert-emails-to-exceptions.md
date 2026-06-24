---
title: Automated purchase order exception creation from emails
description: Emails sent by a registered supplier contact are automatically converted to purchase order exceptions or universal requests by using the Email Intent to Action Agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/convert-emails-to-exceptions.html
release: zurich
topic_type: concept
last_updated: "2026-02-11"
reading_time_minutes: 3
breadcrumb: [Using agentic workflows in Now Assist for Purchase Order Management \(POM\), Now Assist for POM, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Automated purchase order exception creation from emails

Emails sent by a registered supplier contact are automatically converted to purchase order exceptions or universal requests by using the Email Intent to Action Agentic workflow.

The Email Intent to Action Agentic workflow analyzes incoming supplier emails, identifies the email intent, and executes associated actions using the Intent Identification and Intent Executor agents. For more information on the Email Intent to Action Agentic workflow, see [Email Intent to Action Agentic Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/email-agentic-workflow.md).

The workflow can process supplier emails in any of these languages: English, French, Canadian French, German, Japanese, or Dutch.

Suppliers must provide one of the following IDs in their email to identify the relevant purchase order line:

-   ERP purchase order \(PO\) and purchase order line \(POL\) IDs
-   ServiceNow® PO number or ERP PO number when the purchase order contains only one line

## Prerequisites for automated creation of purchase order exceptions

To use this functionality, verify that the following steps are completed:

-   Configure the \[sn\_supplier.slm\_email\] system property. Edit the **Value** field to contain supplier email address. For more information, see [Configure properties for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/config-prop-supp-mgmt.md).

    **Note:** If you plan to use or are using the SLO Supplier inbox for scenarios such as supplier case creation, you must use the same inbox for creating purchase order exceptions.

-   Deactivate the Create Supplier case for email inbound action. For more information, see [Deactivate Create supplier case from email inbound action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/deactivate-create-supplier-case-from-email-inbound-action.md).
-   Activate the Trigger Intent to Action inbound action. To learn how to enable and configure intent to action workflow to invoke the agentic workflow from inbound actions, see [Enable intent to action workflow from inbound actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/enable-intent-to-action.md).
-   Set the **sn\_uni\_req.universal\_request\_portal** property value to **Supplier**. This step supports supplier user experience cases where a supplier email can't be automatically converted to a purchase order exception. Instead, a universal request is created in the Supplier Collaboration Portal and the supplier receives an email with a link to the universal request created. For the link to correctly direct the supplier to the Supplier Collaboration Portal, the **sn\_uni\_req.universal\_request\_portal** property value must be set to **Supplier**.

When a supplier sends an email to the configured email address, the Intent Executor Agent then implements the associated action based on the following conditions:

-   If the email contains a purchase order line related information, a purchase order exception is created.
-   If an email includes details for multiple purchase order lines, separate purchase order exceptions are generated for each line.
-   If the email contains unclear information or questions not related to purchase order exceptions, a universal request is created.
-   If the purchase orders and purchase order lines mentioned by the supplier can't be found in the system, a universal request is created.

The supplier receives an email notification when a purchase order exception or a universal request is created. A banner appears on purchase order exceptions created by the agentic workflow, indicating that an agent created them. The originating email content is added as an entry in the Activity stream, allowing operational buyers to review agent actions and flag any discrepancies.

**Note:**

-   The supplier email must contain one of the following identifiers for the purchase order line:
    -   ERP purchase order \(PO\) and ERP purchase order line \(POL\) IDs
    -   ServiceNow® purchase order line number
    -   ServiceNow® purchase order number when it contains only one line
-   The workflow processes emails in any of these languages: English, French, Canadian French, German, Japanese, or Dutch.

