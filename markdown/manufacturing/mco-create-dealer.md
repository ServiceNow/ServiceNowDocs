---
title: Create dealer
description: Create a dealer role to provide access to MCO capabilities and enable dealers to manage their assigned manufacturing and commercial operations activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-create-dealer.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dealer, Set up MCO, Configure, Manufacturing Commercial Operations]
---

# Create dealer

Create a dealer role to provide access to MCO capabilities and enable dealers to manage their assigned manufacturing and commercial operations activities.

## Before you begin

Role required: manufacturing operations admin \(sn\_mfg\_cmn.manufacturing\_operations\_admin\)

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace.**

2.  Select the List icon.

3.  Navigate to **MCO Setup** &gt; **Dealer**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_vss_54w_vfc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated number of the dealer.**Note:** By default, dealer numbers start with the prefix DLR.

</td></tr><tr><td>

External code

</td><td>

Identifier or reference value from an external system that maps to a corresponding record, process, product, issue type, or transaction. It helps to maintain consistency and traceability when data is exchanged between MCO and third-party systems such as ERP or CRM.

</td></tr><tr><td>

Outbond soap message

</td><td>

Integration mechanism used to send structured SOAP-based requests from MCO to an external system. It typically carries manufacturing or quality-related data—such as issues, investigations, customer complaints, or product records—to another enterprise application for processing, synchronization, or follow-up action.

</td></tr><tr><td>

SOAP message function

</td><td>

Defines the specific web service operation used to send data to an external system and process the response.

</td></tr><tr><td>

Service organization

</td><td>

Service organization that includes internal business locations or channel partners.

</td></tr><tr><td>

Business functions

</td><td>

Business functions of the dealer:-   Sales
-   Sales and service
-   Service only


</td></tr></tbody>
</table>
## Result

The dealer is created.

