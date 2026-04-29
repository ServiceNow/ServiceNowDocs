---
title: Written Statement for Unauthorized Debit \(WSUD\) Troubleshooting
description: This reference topic provides troubleshooting topics for common issues in the Written Statement for Unauthorized Debit \(WSUD\) process. This includes customer signature activities, email notifications, and document verification tasks.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [WSUD, troubleshooting, customer signature, document verification, email, NACHA, ServiceNow]
breadcrumb: [Reference, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Written Statement for Unauthorized Debit \(WSUD\) Troubleshooting

This reference topic provides troubleshooting topics for common issues in the Written Statement for Unauthorized Debit \(WSUD\) process. This includes customer signature activities, email notifications, and document verification tasks.

## Additional troubleshooting information

For the Written Statement for Unauthorized Debit playbook activity for ACH disputes:

-   The `sn_doc_processor.external_user` role is added to `sn_bom.customer` and `sn_bom.consumer`, enabling customers and consumers to view and electronically sign WSUD documents through the portal.
-   The `sn_doc_processor.agent` role is added to `sn_bom_credit_card.dispute_agent` and `sn_bom_credit_card.dispute_agent_connector`, allowing dispute agents and connectors to verify and manage WSUD documents during case review.
-   When transactions are modified in the **Review** lane, the WSUD document is automatically regenerated and a new e-signature link is sent to the customer when the required conditions are met.
-   If the dispute reason code is changed to one that doesn't require a WSUD, the associated Document Verification task created during intake is automatically canceled.

-   **[Customer Signature Required activity not displaying or WSUD verification task not getting generated](../reference/wsud-activity-task-not-generated.md)**  
This reference topic provides troubleshooting steps to resolve the Customer Signature Required activity not appearing in the playbook. It also resolves the Written Statement for Unauthorized Debit \(WSUD\) document verification task not being generated.
-   **[WSUD signing email not sent to customer](../reference/wsud-signing-email-not-sent-to-customer.md)**  
This reference topic provides troubleshooting steps to resolve a Written Statement for Unauthorized Debit \(WSUD\) not being emailed to a customer during ACH dispute intake.
-   **[Unable to sign or submit the WSUD document](../reference/unable-to-sign-or-submit-the-wsud-document.md)**  
This reference topic provides troubleshooting steps to resolve a customer or contact being unable to sign or submit the Written Statement for Unauthorized Debit \(WSUD\) document.
-   **[Upload Document button appears instead of Sign Document button in the WSUD document verification task](../reference/upload-document-instead-of-sign-document.md)**  
This reference topic provides troubleshooting steps to resolve a customer or contact seeing the **Upload Document** button instead of the **Sign Document** button in the **Customer signature required** playbook activity. This activity is for the Written Statement for Unauthorized Debit \(WSUD\) document verification task.

**Parent Topic:**[Dispute management reference](dispute-management-reference.md)

**Related topics**  


[About dispute intake](dispute-intake-overview.md)

[Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md)

