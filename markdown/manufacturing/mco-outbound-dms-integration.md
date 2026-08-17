---
title: Set up outbound DMS integration
description: Send claims, approvals, and status updates from the OEM instance to the connected Dealer Management System \(DMS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-outbound-dms-integration.html
release: australia
topic_type: task
last_updated: "2026-07-13"
reading_time_minutes: 1
keywords: [outbound DMS integration, DMS, SOAP message, WSDL, repair claim, OEM instance, dealer record, business rule, claim adjudication, outbound integration]
breadcrumb: [DMS integration, Integrate, Manufacturing Commercial Operations]
---

# Set up outbound DMS integration

Send claims, approvals, and status updates from the OEM instance to the connected Dealer Management System \(DMS\).

## Before you begin

Role required: admin

## Procedure

1.  Get the WSDL \(Web Services Description Language\) endpoint for the dealer's DMS.

2.  Get the credentials for the dealer's DMS.

3.  Create outbound SOAP \(Simple Object Access Protocol\) message in the sys\_soap\_message table on the OEM ServiceNow instance for this WSDL.

4.  Configure the corresponding SOAP function.

5.  Open the corresponding dealer record from the sn\_dealer\_mgmt\_dealer table.

6.  Update the **Outbound SOAP Message** field with the newly created SOAP message.

7.  Update the **SOAP Message Function** field with the newly created SOAP function.

8.  Verify the business rule conditions that invoke the outbound integration payload on the sn\_repair\_claim\_mgmt\_case table.

    An outbound integration business rule is invoked on the Repair Claim Case table when:

    -   Source = DMS
    -   Claim state changes to a supported adjudication state
    The business rule prepares the outbound payload.

9.  Test claim submissions.

10. Review errors.

11. Push the following changes to the production instance.

    -   Outbound SOAP message
    -   SOAP function
    -   Business rule, if modified
    -   Dealer record changes

