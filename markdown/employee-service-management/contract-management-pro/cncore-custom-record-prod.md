---
title: Create custom record producers for contract requests
description: Copy a base system record producer to create a custom intake form for contract requests, including new contracts, amendments, and renewals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-custom-record-prod.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create custom record producers for contract requests

Copy a base system record producer to create a custom intake form for contract requests, including new contracts, amendments, and renewals.

## Before you begin

Role required: sn\_cm\_core.contract\_config, admin

## About this task

-   Two record producers are available in the base system: Contract request and Contract Amendment and Renewal Request. Copy a base system record producer to reuse its existing configuration settings.
-   The **Type of paper** and **Contract type** variables are mandatory for the workflow to work and must be present in the record producer.
-   The **Signature type** and **Add signatories** variables are also copied from the base record producer.
-   Manually add the following variable sets available in the base system:
    -   Contract request details
    -   Upload Contract Documents
    -   External signatory details

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Filter record producers by setting **Application** to **Contracts Core**.

3.  Open the record producer to copy.

4.  Select **Copy**.

    \[Omitted image "cmpro-sa-custom-rcrd-producer.png"\] Alt text: Copy a base system record producer

5.  In the **Name** field, enter a name for the record producer.

6.  Confirm the **Table name** is set to Contract Request \[sn\_cm\_core\_contract\_request\].

7.  In the Variable Sets related list, add the following variable sets.

    -   Contract request details
    -   Upload Contract Documents
    -   External signatory
8.  Verify that the **Type of paper** and **Contract type** variables are present in the record producer.

9.  Select **Update** to save the record producer.


## Result

The custom record producer is available in the Employee Center.

