---
title: Household form
description: Service Model Foundation uses the Household form to store information about a consumer household, including the household members; relationships created for the household and members; and cases, entitlements, and contracts created for the household and members.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Household form

Service Model Foundation uses the Household form to store information about a consumer household, including the household members; relationships created for the household and members; and cases, entitlements, and contracts created for the household and members.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the household.

</td></tr><tr><td>

Number

</td><td>

The automatically generated number of the household. By default, household numbers start with the prefix HOLD.

</td></tr><tr><td>

Head of household

</td><td>

The consumer in charge of the household.-   When creating a new household record, select a consumer from the Consumer table.
-   When updating an existing household record, select a consumer from the current members of the household.

</td></tr><tr><td>

Street

</td><td>

The street address of the household.

</td></tr><tr><td>

City

</td><td>

The city in which the household resides.

</td></tr><tr><td>

State/Province

</td><td>

The state or province in which the household resides.

</td></tr><tr><td>

Zip/Postal code

</td><td>

The ZIP code or postal code for the household.

</td></tr><tr><td>

Country

</td><td>

The country in which the household resides.

</td></tr><tr><td>

Notes

</td><td>

Additional information about the household.

</td></tr></tbody>
</table>## Household related lists

The Household form includes the following related lists.

<table id="table_wts_433_gmb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current Members

</td><td>

The consumers who are current members of the household.

</td></tr><tr><td>

All Members

</td><td>

Current and past members of a household.As members are added or removed from a household, the member history is retained in this related list.

</td></tr><tr><td>

Member Relationships

</td><td>

Relationships that have been created between members of this household. Member relationships are created using the Authorized Representative responsibility.

 Household members that have an Authorized Representative relationship with another household member can act on behalf of that member and can manage cases for that member.

</td></tr><tr><td>

Household Team

</td><td>

Relationships that have been created between internal users and this household. Household staff relationships are created using the Relationship Manager responsibility.

 Internal users that have a Relationship Manager relationship with a household can manage all of the cases for that household.

</td></tr><tr><td>

Cases

</td><td>

Cases that have been created for this household and the members of this household.

</td></tr></tbody>
</table>**Related topics**  


[Create or update a household](../task/create-consumer-household.md)

