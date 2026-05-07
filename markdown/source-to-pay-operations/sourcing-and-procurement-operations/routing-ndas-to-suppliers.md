---
title: Routing NDAs to suppliers
description: Reduce manual effort by providing your procurement specialist with a single place to perform all the necessary actions when creating and routing Non-Disclosure Agreements \(NDAs\) to suppliers and third parties.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Routing NDAs to suppliers

Reduce manual effort by providing your procurement specialist with a single place to perform all the necessary actions when creating and routing Non-Disclosure Agreements \(NDAs\) to suppliers and third parties.

As a procurement specialist, you can easily define your NDA content and update signer details with the help of a document template that is provided by default with the Document Template plugin \[sn\_doc\], which is added as a dependency on Procurement Case Management \[sn\_spend\_psd\]. The signer details are stored in the Signers table.​

**Note:** You must use the November 2023 version of the Document Template plugin \[sn\_doc\] for using the November 2023 versions of the Procurement Case Management and Playbooks for Sourcing and Procurement Operations plugins.

Further, procurement specialists can easily​ route the NDAs to suppliers and third parties for signing via DocuSign integration, review the signed documents, and close the procurement case of type Send NDA for Signature, from a designated playbook in Source-to-Pay Workspace.

Details of the workflow are provided here.

1.  Define your NDA content and update the list of participants for signature.​ See [Define NDA content and update the list of signers](../task/define-nda-content-update-signers.md).
2.  Set up DocuSign.

    For more information, see [Docusign eSignature Spoke](https://www.servicenow.com/docs/access?context=docusign-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

3.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.
4.  Select the list icon and select **All team work** &gt; **Cases**.
5.  Select **New**.
6.  In the Create a new case dialog box, select **Send NDA for Signature**.
7.  Select **Create Case**.

    **Note:** During a procurement request, when a valid NDA isn’t available for the selected supplier, a procurement case of type Send NDA for Signature is automatically created.

8.  Open the case in Source-to-Pay Workspace, prepare the NDA, and send it for signing to the suppliers and third parties from a playbook.​ See [Send NDA to suppliers for signature](../task/prepare-nda-send-to-signers.md).

    **Note:** If the **Playbook** tab isn’t visible in Source-to-Pay Workspace, verify that the Document Template Integration with DocuSign application is installed correctly.

9.  Sign the NDA.
    -   For external third-party suppliers, [directly sign from the email notification](https://www.youtube.com/watch?v=sFOGy2UwbJk) or from Supplier Collaboration Portal. For more information, see [Using Supplier Collaboration Portal](../../supplier-lifecycle-operations/concept/use-supp-central.md).
    -   For internal supplier representatives, from Employee Center. For more information, see [Sign a document using DocuSign from Employee Center](../task/sign-document-task-ec.md).
10. Review the signatures from the playbook in Source-to-Pay Workspace, notify the user, and close the case. See [Send NDA to suppliers for signature](../task/prepare-nda-send-to-signers.md).

## Additional configurations

You can make changes to the Send NDA for signature playbook, if you must, from Playbooks.

For adding new participants, create a new column on the procurement case and update the logic to populate in Playbooks. For more information, refer to the implementation of the signer\_1 column.

You can also update the subflows to incorporate any new logic. Flow details can be found in different steps in Playbooks.

-   **[Define NDA content and update the list of signers](../task/define-nda-content-update-signers.md)**  
As a procurement specialist, you can easily define your Non-Disclosure Agreement \(NDA\) content and update the list of participants for whose signature is required.
-   **[Send NDA to suppliers for signature](../task/prepare-nda-send-to-signers.md)**  
As a procurement specialist, you can use playbooks to prepare a Non-Disclosure Agreement \(NDA\) and send it for signing to the suppliers and third parties and review the signed and completed NDA.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook](../task/process-purchase-order.md)

[Process a purchase requisition edit request in playbook](../task/playbook-edit-request-flow.md)

[Process a return request in playbook](../task/playbook-return-request.md)

[Process a replacement request in playbook](../task/playbook-replacement-request.md)

[Process an edit receipt request in playbook](../task/playbook-process-edit-receipt.md)

[Fulfilling request for copy of contract in playbook](fulfilling-request-for-contract.md)

[Verifying delivery addresses in playbook](delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](general-ledger-details-in-playbook.md)

[Sourcing intake guided experience with playbooks](sourcing-intake-guided-exp.md)

[Streamlining the supplier risk assessment workflow](simplify-risk-assessment-wf.md)

