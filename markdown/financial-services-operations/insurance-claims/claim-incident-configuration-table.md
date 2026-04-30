---
title: Claim Incident Configuration table
description: Associate the service definition of a case with the incident and adjuster task service definitions by using the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table in the Insurance claims application.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-10-10"
reading_time_minutes: 2
breadcrumb: [Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Claim Incident Configuration table

Associate the service definition of a case with the incident and adjuster task service definitions by using the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table in the Insurance claims application.

## Claim Incident Configuration table overview

You can define the claim incidents that can be created in the Insurance claims workflow by making an entry in the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table. This incident type also creates an adjuster task in the system for the corresponding case so that you don't have to notify the adjuster about the case.

To access the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table, set the application scope of your instance to **Insurance claims**, and then navigate to **All** &gt; **Insurance claims** &gt; **Administration** &gt; **Claim incident configurations**.

The following example shows the table fields of the Claim Incident Configuration \(sn\_ins\_claim\_incident\_config\) table. For more information, see the next section.![Claim Incident Configuration table in Insurance claims.](../image/claim-incident-configurations-table.png)

## Claim Incident Configuration Table fields

The following table shows the fields in the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table.

<table id="table_o5f_jk5_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the claim incident configuration entry.

</td></tr><tr><td>

Active

</td><td>

Status of whether this incident is active or inactive and whether the incident displays in the first notice of loss playbook.

</td></tr><tr><td>

Adjuster task service definition

</td><td>

Adjuster task service definition \(that is, a service definition that creates an adjuster task in a claim\). For more information, see [Create a service definition for Insurance claims](../task/create-a-service-definition-for-insurance-claims.md).

</td></tr><tr><td>

Create adjuster task

</td><td>

How an adjuster task is generated:-   Per incident: Creates an adjuster task for each incident.
-   Per incident type: Creates an adjuster task for each incident type \(for example, one task for all trip incidents and another task for all baggage incidents\).

</td></tr><tr><td>

Incident table name

</td><td>

Table in which the incidents are stored. For more information, see [Claim incidents](claim-incidents.md).

</td></tr><tr><td>

Incident type icon

</td><td>

Icon that displays in the playbook for the claim incident.

</td></tr><tr><td>

Itemized loss available

</td><td>

Whether the claim incident supports itemizing each loss \(for example, to itemize each item in a baggage claim\).

</td></tr><tr><td>

Order

</td><td>

Order in which the service definition appears in the playbook.

</td></tr><tr><td>

Service definition

</td><td>

Service definition for the case \(for example, Report travel claim\). For more information, see [Creating a service definition for Insurance claims](create-service-definitions-for-insurance-claims.md).

</td></tr><tr><td>

Short description

</td><td>

Brief description of the claim incident, which is also displayed in the playbook.

</td></tr></tbody>
</table>## Travel insurance example of the Claim Incident Configuration table

In the following travel insurance line of business \(LOB\) example, the claim incident configuration is reflected in the workflow when reporting a travel claim. The **Incident details** activity in the first notice of loss playbook shows the entries in the table and information about each entry.

![Entries in the Claim Incident Configuration table that can be seen in the Incident details activity.](../image/fnol-incident-details.png)

If the claim incident supports an itemized loss as defined in the table, the **Itemized Loss/Expenses** tab is also displayed when the incident is saved as shown in the following example.

![Itemized Loss/Expenses tab is displayed for an incident when the Itemized loss available is true.](../image/incident-itemized-loss.png)

