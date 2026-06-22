---
title: Send a non-disclosure agreement document for signature
description: After a non-disclosure agreement contract document has been reviewed and finalized, send the document for signature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-service-delivery/snlc-send-doc-sign-nda.html
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Send a non-disclosure agreement document for signature

After a non-disclosure agreement contract document has been reviewed and finalized, send the document for signature.

## Before you begin

The contract document must have been reviewed and finalized, and the contract status must be set to Document ready. For more information, see and [Review a contract document in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-submit-req-chngs-ndar.md) and [Work on a contract change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-finalize-document-nda.md).

Role required: sn\_cm\_core.contract\_user and sn\_lg\_ops.legal\_user

## Procedure

1.  Open a legal request.

<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d151993e68">

Method

</th><th align="left" id="d151993e71">

Actions

</th></tr></thead><tbody><tr><td id="d151993e77">

**__Employee Center__**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**
2.  Select **My Requests** option on the header menu.
3.  Open your submitted non-disclosure agreement request.


</td></tr><tr><td id="d151993e110">

**__Legal Service Portal__**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**
2.  Select **My Requests** option on the header menu.
3.  Select **View all requests**.
4.  Open your submitted non-disclosure agreement request.


</td></tr></tbody>
</table>2.  Select the **Contract documents** tab.

3.  Select **Send for signature**.

    **Note:** If a message states that the signatories are not in sync, update and sync them before sending the document for signature.

    -   If you are using Contract Management Pro 1.2.1, see [Resolve the failure to send contract documents for signature \(starting Contract Management Pro 1.2.1\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-sync-doc-user.md).
    -   If you are using an earlier version of Contract Management Pro, see [Resolve an error during send for signature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-sync-signatories-user.md).
    A message appears displaying details of the contract document that is sent for signature.

4.  Select **Send for signature** on the confirmation message.


## Result

The document is sent for signature to the specified signatories. The activity stream displays details of the contract document that is sent for signature.

The contract state and contract status updates to Awaiting Signature. For more information, see [Signature workflow for a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-lsd-signature-workflow.md).

**Parent Topic:**[Work on NDA legal requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-work-on-contract-request.md)

