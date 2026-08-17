---
title: Set up inbound DMS integration
description: Route dealer records, orders, and updates from the dealer management system \(DMS\) into the original equipment manufacturer \(OEM\) instance \(DMS to OEM ServiceNow instance\) for processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-configure-dms.html
release: australia
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 2
keywords: [DMS integration, SOAP API, repair claims, warranty claims, data mapping]
breadcrumb: [DMS integration, Integrate, Manufacturing Commercial Operations]
---

# Set up inbound DMS integration

Route dealer records, orders, and updates from the dealer management system \(DMS\) into the original equipment manufacturer \(OEM\) instance \(DMS to OEM ServiceNow instance\) for processing.

## Before you begin

Repair Claim Management plugin must be installed.

Role required: admin

## About this task

Integrating your DMS with MCO enables real-time synchronization of warranty and repair claim data. This integration streamlines claim creation, status tracking, and data validation across both systems, reducing manual data entry and improving claim accuracy.

## Procedure

1.  Install the integration application, MCO Integration \(sn\_mco\_integ\).

    This application provides the STAR \(Standards for Technology in Automotive Retail\)-compliant SOAP integration layer. It is used to exchange repair order and service advisory information with external dealer systems.

2.  Create the integration user.

    Create a dedicated integration user for the DMS provider or integration middleware. Assign only the roles required to access the SOAP endpoint and the repair claim tables used by the integration.

3.  Assign the role sn\_repr\_claim\_mgmt.soap\_integration\_repair\_claim to the integration user.

4.  Configure authentication and access.

    Work with the DMS provider to configure the required authentication method, credentials, network allowlists, and any certificate or security requirements for inbound and outbound SOAP traffic.

5.  Share the WSDL endpoint details with the dealer's DMS.

    Provide the DMS provider with the Warranty Claims SOAP API WSDL, endpoint URL, supported operation details, and sample request and response payloads for the target MCO instance.

6.  Map STAR XML payloads to MCO records.

    Review the configuration-driven adapters and confirm how STAR repair order fields map to the Repair Claim Case, Repair Claim Case Line, and Repair Claim Case Line Charge tables.

7.  Validate reference data.

    Confirm that incoming values from the DMS match the corresponding reference data in MCO. Values to check include dealer identifiers, repair order numbers, VIN or serial numbers, labor codes, parts, and charge types.

8.  Test claim submissions.

    Send a sample STAR-compliant repair order from the DMS or test client. Verify that MCO creates the warranty or repair claim case with the expected case lines and line charges.

9.  Test claim status updates.

    Process the claim in MCO and verify that approval, rejection, return, adjudication, or service advisory responses are generated and returned to the DMS as expected.

10. Review error handling.

    Test missing, invalid, and unmatched data scenarios to confirm that SOAP faults, validation errors, and integration logs provide sufficient information for troubleshooting.

11. Migrate the configuration to production.

    After successful end-to-end testing, update production endpoint details, rotate credentials if required, and monitor the first set of live transactions.


**Related topics**  


[Set up outbound DMS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-outbound-dms-integration.md)

[MCO Integration APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-integrate.md)

