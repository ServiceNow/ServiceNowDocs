---
title: Cancel a legal request
description: Cancel a legal contract request if it is no longer necessary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-service-delivery/snlc-cancel-request-tpc.html
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Cancel a legal request

Cancel a legal contract request if it is no longer necessary.

## Before you begin

**Important:** Cancelling a legal contract request after it has been sent for signature stops the process in its current state.

Role required: sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user, sn\_lg\_cnt.contract\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**.

2.  Open your submitted legal request from the **My Requests** option on the header menu.

3.  On the Standard Ticket page, from the Actions menu, select **Cancel Request**.

4.  In the dialog box, enter comments to explain why the request was canceled.

5.  Select **Confirm Cancellation**.


## Result

-   The request is canceled and the associated active flows are terminated. The cancellation comments appear in the **Activity** tab of the request.
-   The Contract status changes to Contract cancelled.
-   The document signature sent to signatories is canceled to block further signing. The signatories get an email notification that the legal request has been canceled.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement requests]()

[Third-party contract review requests]()

[Contract amendments]()

[Linking parent-child contracts]()

[Internal review overview]()

[Signature workflow for a request]()

[View and download a signed contract document]()

[View contract requests]()

[Manage Contract Management Pro for Legal Service Delivery]()

