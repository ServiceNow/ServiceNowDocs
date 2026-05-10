---
title: Automated purchase order exception creation from emails
description: Emails sent by a registered supplier contact are automatically converted to purchase order exceptions or universal requests by using the Email Intent to Action Agentic workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using agentic workflows in Now Assist for Purchase Order Management \(POM\), Now Assist for POM, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Automated purchase order exception creation from emails

Emails sent by a registered supplier contact are automatically converted to purchase order exceptions or universal requests by using the Email Intent to Action Agentic workflow.

The Email Intent to Action Agentic workflow analyzes incoming supplier emails, identifies the email intent, and executes associated actions using the Intent Identification and Intent Executor agents. For more information on the Email Intent to Action Agentic workflow, see [Email Intent to Action Agentic Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/email-agentic-workflow.md).

## Prerequisites for automated creation of purchase order exceptions

To use this functionality, verify that the following steps are completed:

-   Configure the \[sn\_supplier.slm\_email\] system property and edit the **Value** field to contain supplier email address. For more information, see [Configure properties for Supplier Case Management](../../supplier-lifecycle-operations/reference/config-prop-supp-mgmt.md).

    **Note:** If you plan to use or are using the SLO Supplier inbox for scenarios such as supplier case creation, you must use the same inbox for creating purchase order exceptions.

-   Deactivate the Create Supplier case for email inbound action. For more information, see [Deactivate Create supplier case from email inbound action](../../supplier-lifecycle-operations/concept/deactivate-create-supplier-case-from-email-inbound-action.md).
-   Activate the Trigger Intent to Action inbound action. To learn how to enable and configure intent to action workflow to invoke the agentic workflow from inbound actions, see [Enable intent to action workflow from inbound actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/enable-intent-to-action.md).
-   Set the **sn\_uni\_req.universal\_request\_portal** property value to **Supplier**. This step supports supplier user experience cases where a supplier email cannot be automatically converted to a purchase order exception. Instead, a universal request is created in the Supplier Collaboration Portal and the supplier receives an email with a link to the universal request created. For the link to correctly direct the supplier to the Supplier Collaboration Portal, the **sn\_uni\_req.universal\_request\_portal** property value must be set to **Supplier**.

When a supplier sends an email to the configured email address, the Intent Executor Agent then implements the associated action based on the following conditions:

-   If the email contains a purchase order line related information, a purchase order exception is created.
-   If the email contains purchase order exception information related to different purchase order lines, multiple purchase order exceptions are created.
-   If the email contains vague information or queries unrelated to purchase order exceptions, a universal request is created.
-   If the purchase orders and purchase order lines mentioned by the supplier cannot be found in the system, a universal request is created.
-   If the sender of the email is not a registered supplier contact, an automated email reply is sent requesting them to register.
-   If the sender is mapped to several suppliers, an automated email reply is sent to request clarification.

The supplier receives an email notification when a purchase order exception or a universal request is created. A banner appears on purchase order exceptions created by the agentic workflow, indicating that an agent created them. The originating email content is added as an entry in the Activity stream, allowing operational buyers to review agent actions and flag any discrepancies.

**Note:**

-   The supplier email must include a ServiceNow® purchase order line number \(and not the ERP purchase order line number\) for the workflow to associate it with the corresponding record.
-   The workflow only processes emails that are in English.

**Parent Topic:**[Using agentic workflows in Now Assist for Purchase Order Management \(POM\)](using-agentic-wf-na-for-pom.md)

**Related topics**  


[Identify and execute mitigation strategies for purchase order exceptions](mitigation-strategies-for-po-exceptions.md)

