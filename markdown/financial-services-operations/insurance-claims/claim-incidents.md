---
title: Claim incidents
description: You can create a Claim Incident \[sn\_ins\_claim\_property\] table that records the details of a particular claim in the Insurance claims application.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Claim incidents

You can create a Claim Incident \[sn\_ins\_claim\_property\] table that records the details of a particular claim in the Insurance claims application.

The Insurance claims application includes four incident tables in the base system:

-   Claim incident \[sn\_ins\_claim\_property\] table
-   Baggage incident \[sn\_ins\_claim\_baggage\] table
-   Trip incident \[sn\_ins\_claim\_trip\] table
-   Injury incident \[sn\_ins\_claim\_injury\] table

These tables contain the fields that are specific to their incident types.

You can use an existing table to store incidents for your claims process, or you can create a new incident table. For example, your workflow may need to handle different incident types, such as property damage, medical emergencies, or environmental claims. You can create and configure custom incident tables that are tailored to those specific incident types.

After creating the incident table, you can define the relationship of the table with the respective service definition by using the [Claim Incident Configuration table](claim-incident-configuration-table.md).

**Related topics**  


[Claim Incident Configuration table](claim-incident-configuration-table.md)

[Components installed with Insurance claims](../reference/components-installed-with-insurance-claims-flow.md)

[Insurance Claims Core tables](../../fso-common/reference/insurance-claims-core-tables.md)

