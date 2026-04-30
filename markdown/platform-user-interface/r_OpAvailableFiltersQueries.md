---
title: Operators available for filters and queries
description: The system provides a set of operators for use with filters, condition builders, and encoded queries. The data type of a field determines what operators are available for it.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Operators available for filters and queries

The system provides a set of operators for use with filters, condition builders, and encoded queries. The data type of a field determines what operators are available for it.

## Operators available for condition builders

<table id="table_jb1_r21_ft"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

AND

</td><td>

\[Active\]\[is\]\[True\]\[AND\]\[Caller\]\[is not empty\]

</td><td>

^

</td><td>

active=true^CallerISNOTEMPTY

</td><td>

All records that have both of the following:-   **Active** field is **True**
-   **Caller** field has any value

</td></tr><tr><td>

OR condition

</td><td>

\[Short description\]\[is empty\]\[OR\]\[Description\]\[is empty\]

</td><td>

^OR

</td><td>

short\_descriptionISEMPTY^ORdescriptionISEMPTY

</td><td>

All records that have at least one of the following:-   **Short description** field has no value
-   **Description** field has no value

</td></tr><tr><td>

OR filter

</td><td>

All these conditions must be met

 \[Short description\]\[is empty\]

 OR all these conditions must be met

 \[Description\]\[is not empty\]

</td><td>

^NQ

 new query

</td><td>

short\_descriptionISEMPTY^NQdescriptionISNOTEMPTY

</td><td>

All records that have at least one of the following:-   **Short description** field has no value
-   **Description** field has no value

</td></tr></tbody>
</table>## Operators available for string fields

<table id="table_egn_qcy_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

starts with

</td><td>

\[Short description\]\[starts with\]\[SAP\]

</td><td>

STARTSWITH

</td><td>

short\_descriptionSTARTSWITHSAP

</td><td>

All records in which the characters "SAP" appear at the beginning of the value for the **Short description** field.

</td></tr><tr><td>

ends with

</td><td>

\[Short description\]\[ends with\]\[outage\]

</td><td>

-   %
-   ENDSWITH

</td><td>

short\_descriptionENDSWITHoutage

</td><td>

All records in which the string "outage" appears at the end of the value for the **Short description** field.

</td></tr><tr><td>

contains

</td><td>

\[Short description\]\[contains\]\[SAP\]

</td><td>

-   \*
-   LIKE

</td><td>

short\_descriptionLIKESAP

</td><td>

All records in which the characters "SAP" appear anywhere in the value for the **Short description** field.

</td></tr><tr><td>

does not contain

</td><td>

\[Short description\]\[does not contain\]\[SAP\]

</td><td>

-   !\*
-   NOT LIKE

</td><td>

short\_descriptionNOT LIKESAP

</td><td>

All records in which the characters "SAP" do not appear anywhere in the value for the **Short description** field.

</td></tr><tr><td>

is

</td><td>

\[Short description\]\[is\]\[Network storage unavailable\]

</td><td>

=

</td><td>

short\_description=Network storage unavailable

</td><td>

All records in which the **Short description** says nothing else but "Network storage is unavailable."

</td></tr><tr><td>

is not

</td><td>

\[Short description\]\[is not\]\[Network storage unavailable\]

</td><td>

!=

</td><td>

short\_description!=Network storage unavailable

</td><td>

All records in which the value for the **Short description** field says anything but "Network storage is unavailable."

</td></tr><tr><td>

is empty

</td><td>

\[Short description\]\[is empty\]

</td><td>

ISEMPTY

</td><td>

short\_descriptionISEMPTY

</td><td>

All records in which there is no value in the **Short description** field.

</td></tr><tr><td>

is not empty

</td><td>

\[Short description\]\[is not empty\]

</td><td>

ISNOTEMPTY

</td><td>

short\_descriptionISNOTEMPTY

</td><td>

All records in which there is any value in the **Short description** field.

</td></tr><tr><td>

is anything

</td><td>

\[Short description\]\[is anything\]

</td><td>

ANYTHING

</td><td>

short\_descriptionANYTHING

</td><td>

All records in which the **Short description** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is empty string

</td><td>

\[Short description\]\[is empty string\]

</td><td>

EMPTYSTRING

</td><td>

short\_descriptionEMPTYSTRING

</td><td>

All records in which there is no value in the **Short description** field.

</td></tr><tr><td>

less than or is

</td><td>

\[Short description\]\[less than or is\]\[s\]

</td><td>

&lt;=

</td><td>

short\_descriptionlt;=s

</td><td>

All records in which the string in the **Short description** field is one of the following:-   the first letter is any letter between "a" and "s"
-   the exact value is "s"

</td></tr><tr><td>

greater than or is

</td><td>

\[Short description\]\[greater than or is\]\[s\]

</td><td>

&gt;=

</td><td>

short\_description&gt;=s

</td><td>

All records in which the string in the **Short description** field is one of the following:-   the first letter is any letter between "s" and "z"
-   the exact value is "s"

</td></tr><tr><td>

between

</td><td>

\[Short description\]\[between\]\[q\] and \[t\]

</td><td>

BETWEEN

</td><td>

short\_descriptionBETWEENq@t

</td><td>

All records in which the first letter in the **Short description** field is "q," "r," "s," or "t."

</td></tr><tr><td>

is same

</td><td>

\[Short description\]\[is same\] as \[Description\]

</td><td>

SAMEAS

</td><td>

short\_descriptionSAMEASdescription

</td><td>

All records in which there exist matching values for the **Short description** and **Description** fields.

</td></tr><tr><td>

is different

</td><td>

\[Short description\]\[is different\] from \[Description\]

</td><td>

NSAMEAS

</td><td>

short\_descriptionNSAMEASdescription

</td><td>

All records in which there exist differing values for the **Short description** and **Description** fields.

</td></tr></tbody>
</table>## Operators available for reference fields

<table id="table_cz1_q2y_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

is

</td><td>

\[Caller\]\[is\]\[Don Goodliffe\]

</td><td>

=

</td><td>

caller\_id=9ee1b13dc6112271007f9d0efdb69cd0

</td><td>

All records in which the **Caller** is no one else but Don Goodliffe.

</td></tr><tr><td>

is not

</td><td>

\[Caller\]\[is not\]\[Don Goodliffe\]

</td><td>

!=

</td><td>

caller\_id!=9ee1b13dc6112271007f9d0efdb69cd0

</td><td>

All records in which the **Caller** field is populated by any user record but Don Goodliffe.

</td></tr><tr><td>

is empty

</td><td>

\[Caller\]\[is empty\]

</td><td>

ISEMPTY

</td><td>

caller\_idISEMPTY

</td><td>

All records in which the **Caller** field has no value.

</td></tr><tr><td>

is not empty

</td><td>

\[Caller\]\[is not empty\]

</td><td>

ISNOTEMPTY

</td><td>

caller\_idISNOTEMPTY

</td><td>

All records in which there is any value in the **Caller** field.

</td></tr><tr><td>

starts with

</td><td>

\[Caller\]\[starts with\]\[Don\]

</td><td>

STARTSWITH

</td><td>

caller\_idSTARTSWITHDon

</td><td>

All records in which the name in the **Caller** field begins with "Don."

</td></tr><tr><td>

ends with

</td><td>

\[Caller\]\[ends with\]\[liffe\]

</td><td>

-   %
-   ENDSWITH

</td><td>

caller\_idENDSWITHliffe

</td><td>

All records in which the name in the **Caller** field has the letters "liffe" at the end.

</td></tr><tr><td>

contains

</td><td>

\[Caller\]\[contains\]\[on\]

</td><td>

-   \*
-   LIKE

</td><td>

caller\_idLIKEon

</td><td>

All records in which the characters "on" appear anywhere in the name for the **Caller** field.

</td></tr><tr><td>

does not contain

</td><td>

\[Caller\]\[does not contain\]\[on\]

</td><td>

-   !\*
-   NOTLIKE

</td><td>

caller\_idNOT LIKEon

</td><td>

All records in which the characters "on" do not appear anywhere in the name for the **Caller** field.

</td></tr><tr><td>

is anything

</td><td>

\[Caller\]\[is anything\]

</td><td>

ANYTHING

</td><td>

caller\_idANYTHING

</td><td>

All records in which the **Caller** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[Caller\]\[is same\] as \[Assigned to\]

</td><td>

SAMEAS

</td><td>

caller\_idSAMEASassigned\_to

</td><td>

All records in which the same user record is referenced in the **Caller** and **Assigned to** fields.

</td></tr><tr><td>

is different

</td><td>

\[Caller\]\[is different\] from \[Assigned to\]

</td><td>

NSAMEAS

</td><td>

caller\_idNSAMEASassigned\_to

</td><td>

All records in which the user records in the **Caller** and **Assigned to** fields do no match.

</td></tr><tr><td>

is empty string

</td><td>

\[Caller\]\[is empty string\]

</td><td>

EMPTYSTRING

</td><td>

caller\_idEMPTYSTRING

</td><td>

All records in which the **Caller** field has no value.

</td></tr><tr><td>

is \(dynamic\)

</td><td>

\[Caller\]\[is \(dynamic\)\]\[Me\]

</td><td>

DYNAMIC

</td><td>

caller\_idDYNAMIC54635e965f510100a9ad2572f2b4774c

</td><td>

All records in which your user record populates the **Caller** field.

</td></tr><tr><td>

is in hierarchy

</td><td>

\[Manager\]\[is in hierarchy\]\[Manager Hierarchy\] starting at \[Don Goodliffe\] which is \[Included\]

</td><td>

IN\_HIERARCHY

</td><td>

managerIN\_HIERARCHYfdd0fa0f93f5d2505bd0bd886cba1015%409ee1b13dc6112271007f9d0efdb69cd0

</td><td>

All records throughout the Manager hierarchy in which the manager is Don Goodliffe or a user reporting up to Don Goodliffe.

</td></tr><tr><td>

is in hierarchy \(dynamic\)

</td><td>

\[Manager\]\[is in hierarchy \(dynamic\)\]\[Manager Hierarchy\] starting at \[Me\] which is \[Included\]

</td><td>

IN\_HIERARCHY\_DYNAMIC

</td><td>

managerIN\_HIERARCHY\_DYNAMICfdd0fa0f93f5d2505bd0bd886cba1015%4090d1921e5f510100a9ad2572f2b477fe

</td><td>

All records throughout the Manager hierarchy in which the manager is you or a user reporting up to you.**Note:** A record hierarchy between related records in the same table must be established before you can use this operator. See [Building hierarchical queries](https://www.servicenow.com/docs/access?context=data-hierarchies&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Note:** Not all operators are available for all reference types. Depending on the reference you select, you may see a shorter list of operators.

## Operators available for choice fields containing strings

<table id="table_mjd_4fy_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

is

</td><td>

\[Subcategory\]\[is\]\[Email\]

</td><td>

=

</td><td>

subcategory=email

</td><td>

All records in which the **Subcategory** is nothing else but **Email**.

</td></tr><tr><td>

is not

</td><td>

\[Subcategory\]\[is not\]\[Email\]

</td><td>

!=

</td><td>

subcategory!=email

</td><td>

All records in which the **Subcategory** field is populated by any value except **Email**.

</td></tr><tr><td>

is one of

</td><td>

\[Subcategory\]\[is one of\]\[DB2, MS SQL Server, Oraclel\]

</td><td>

IN

</td><td>

subcategoryINdb2,sql server,oracle

</td><td>

All records in which the **Subcategory** field is populated by one of the following values:-   DB2
-   MS SQL Server
-   Oraclel

</td></tr><tr><td>

is not one of

</td><td>

\[Subcategory\]\[is not one of\]\[DB2, MS SQL Server, Oraclel\]

</td><td>

NOT IN

</td><td>

subcategoryNOT INdb2,sql server,oracle

</td><td>

All records in which the **Subcategory** field is populated by anything except the following values:-   DB2
-   MS SQL Server
-   Oraclel

</td></tr><tr><td>

contains

</td><td>

\[Subcategory\]\[contains\]\[Em\]

</td><td>

LIKE

</td><td>

subcategoryLIKEem

</td><td>

All records in which the characters "Em" appear anywhere in the value for the **Subcategory** field.

</td></tr><tr><td>

starts with

</td><td>

\[Subcategory\]\[starts with\]\[Em\]

</td><td>

STARTSWITH

</td><td>

subcategorySTARTSWITHem

</td><td>

All records in which the characters "Em" appear at the beginning of the value for the **Subcategory** field.

</td></tr><tr><td>

ends with

</td><td>

\[Subcategory\]\[ends with\]\[il\]

</td><td>

-   %
-   ENDSWITH

</td><td>

subcategoryENDSWITHil

</td><td>

All records in which the characters "il" appear at the end of the value for the **Subcategory** field.

</td></tr><tr><td>

does not contain

</td><td>

\[Subcategory\]\[does not contain\]\[Em\]

</td><td>

NOT LIKE

</td><td>

subcategoryNOT LIKEem

</td><td>

All records in which the characters "Em" do not appear anywhere in the value for the **Subcategory** field.

</td></tr><tr><td>

is anything

</td><td>

\[Subcategory\]\[is anything\]

</td><td>

ANYTHING

</td><td>

subcategoryANYTHING

</td><td>

All records in which the **Subcategory** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[Subcategory\]\[is same\] as \[Category\]

</td><td>

SAMEAS

</td><td>

subcategorySAMEAScategory

</td><td>

All records in which there exist matching values for the **Subcategory** and **Category** fields.

</td></tr><tr><td>

is different

</td><td>

\[Subcategory\]\[is different\] from \[Category\]

</td><td>

NSAMEAS

</td><td>

subcategoryNSAMEAScategory

</td><td>

All records in which there exist differing values for the **Subcategory** and **Category** fields.

</td></tr></tbody>
</table>## Operators available for choice fields containing integers

<table id="table_b5h_hgy_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

is

</td><td>

\[Impact\]\[is\]\[1 - High\]

</td><td>

=

</td><td>

impact=1

</td><td>

All records in which the value in the **Impact** field is nothing else but **1 - High**.

</td></tr><tr><td>

is not

</td><td>

\[Impact\]\[is not\]\[1 - High\]

</td><td>

!=

</td><td>

impact!=1

</td><td>

All records in which the value in the **Impact** field is anything but **1 - High**.

</td></tr><tr><td>

is one of

</td><td>

\[Impact\]\[is one of\]\[1 - High, 2 - Medium\]

</td><td>

IN

</td><td>

impactIN1,2

</td><td>

All records in which the **Impact** field is populated by one of the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

is not one of

</td><td>

\[Impact\]\[is not one of\]\[1 - High, 2 - Medium\]

</td><td>

NOT IN

</td><td>

impactNOT IN1,2

</td><td>

All records in which the **Impact** field is populated by anything except the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

is empty

</td><td>

\[Impact\]\[is empty\]

</td><td>

EMPTY

</td><td>

impactISEMPTY

</td><td>

All records in which the **Impact** field has no value.

</td></tr><tr><td>

is not empty

</td><td>

\[Impact\]\[is not empty\]

</td><td>

NOTEMPTY

</td><td>

impactISNOTEMPTY

</td><td>

All records in which the **Impact** field has any value.

</td></tr><tr><td>

less than

</td><td>

\[Impact\]\[less than\]\[2 - Medium\]

</td><td>

&lt;

</td><td>

impact&lt;2

</td><td>

All records in which the **Impact** field has a value of **1 - High**.

</td></tr><tr><td>

greater than

</td><td>

\[Impact\]\[greater than\]\[2 - Medium\]

</td><td>

&gt;

</td><td>

impact&gt;2

</td><td>

All records in which the **Impact** field has a value of **3 - Low**

</td></tr><tr><td>

less than or is

</td><td>

\[Impact\]\[less than or is\]\[2 - Medium\]

</td><td>

&lt;=

</td><td>

impact&lt;=2

</td><td>

All records in which the **Impact** field has a value of **1 - High** or **2 - Medium**.

</td></tr><tr><td>

greater than or is

</td><td>

\[Impact\]\[greater than or is\]\[2 - Medium\]

</td><td>

&gt;=

</td><td>

impact&gt;=2

</td><td>

All records in which the **Impact** field has a value of **2 - Medium** or **3 - Low**.

</td></tr><tr><td>

between

</td><td>

\[Impact\]\[between\]\[1 - High\] and \[3 - Low\]

</td><td>

BETWEEN

</td><td>

impactBETWEEN1@2

</td><td>

All records in which the **Impact** field has one of the following values:-   **1 - High**
-   **2 - Medium**
-   **3 - Low**

.

</td></tr><tr><td>

is anything

</td><td>

\[Impact\]\[is anything\]

</td><td>

ANYTHING

</td><td>

impactANYTHING

</td><td>

All records in which the **Impact** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[Impact\]\[is same\] as \[Urgency\]

</td><td>

SAMEAS

</td><td>

impactSAMEASurgency

</td><td>

All records in which there exist matching values for the **Impact** and **Urgency** fields.

</td></tr><tr><td>

is different

</td><td>

\[Impact\]\[is different\] from \[Urgency\]

</td><td>

NSAMEAS

</td><td>

impactNSAMEASurgency

</td><td>

All records in which there exist differing values for the **Impact** and **Urgency** fields.

</td></tr></tbody>
</table>**Note:** The operators ‘less than or is’ and ‘greater than or is’ are not supported for integer fields in the condition builder. Use a scripted condition instead.

## Operators available for date-time fields

<table id="table_url_chy_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

on

</td><td>

\[SLA due\]\[on\]\[Today\]

</td><td>

ONToday

</td><td>

sla\_dueONToday@javascript:gs.daysAgoStart\(0\)@javascript:gs.daysAgoEnd\(0\)

</td><td>

All records in which the value for the **SLA due** field matches the date for today.

</td></tr><tr><td>

not on

</td><td>

\[SLA due\]\[not on\]\[Today\]

</td><td>

NOTONToday

</td><td>

sla\_dueNOTONToday@javascript:gs.daysAgoStart\(0\)@javascript:gs.daysAgoEnd\(0\)

</td><td>

All records in which the value for the **SLA due** field is any other date but today.

</td></tr><tr><td>

before

</td><td>

\[SLA due\]\[before\]\[Today\]

</td><td>

&lt;

</td><td>

sla\_due&lt;javascript:gs.daysAgoStart\(0\)

</td><td>

All records in which the value for the **SLA due** field is any date previous to today.

</td></tr><tr><td>

at or before

</td><td>

\[SLA due\]\[at or before\]\[Today\]

</td><td>

&lt;=

</td><td>

sla\_due&lt;=javascript:gs.daysAgoEnd\(0\)

</td><td>

All records in which the value for the **SLA due** field is one of the following:-   any date previous to today
-   today

</td></tr><tr><td>

after

</td><td>

\[SLA due\]\[after\]\[Today\]

</td><td>

&gt;

</td><td>

sla\_due&gt;javascript:gs.daysAgoEnd\(0\)

</td><td>

All records in which the value for the **SLA due** field is any date after today.

</td></tr><tr><td>

at or after

</td><td>

\[SLA due\]\[at or after\]\[Today\]

</td><td>

&gt;=

</td><td>

sla\_due&gt;=javascript:gs.daysAgoStart\(0\)

</td><td>

All records in which the date value for the **SLA due** field is one of the following:-   today
-   any date after today

</td></tr><tr><td>

between

</td><td>

\[SLA due\]\[between\]\[Yesterday\] and \[Today\]

</td><td>

BETWEEN

</td><td>

sla\_dueBETWEENjavascript:gs.daysAgoStart\(1\)@javascript:gs.daysAgoEnd\(0\)

</td><td>

All records in which the value for the **SLA due** field is either yesterday's or today's date.

</td></tr><tr><td>

trend \(on or after\)

</td><td>

\[SLA due\]\[trend\]\[on or after\]\[Monday\]

</td><td>

DATEPART

</td><td>

sla\_dueDATEPARTMonday@javascript:gs.datePart\('dayofweek','monday','GE'\)

</td><td>

All records in which the date in the **SLA due** field is on any day of the week except a Sunday.

</td></tr><tr><td>

trend \(on or before\)

</td><td>

\[SLA due\]\[trend\]\[on or before\]\[Monday\]

</td><td>

DATEPART

</td><td>

sla\_dueDATEPARTMonday@javascript:gs.datePart\('dayofweek','monday','LE'\)

</td><td>

All records in which the date in the **SLA due** field is on either a Sunday or a Monday.

</td></tr><tr><td>

trend \(after\)

</td><td>

\[SLA due\]\[trend\]\[after\]\[Monday\]

</td><td>

DATEPART

</td><td>

sla\_dueDATEPARTMonday@javascript:gs.datePart\('dayofweek','monday','GT'\)

</td><td>

All records in which the date in the **SLA due** field is on any day of the week except a Sunday or a Monday.

</td></tr><tr><td>

trend \(before\)

</td><td>

\[SLA due\]\[trend\]\[before\]\[Monday\]

</td><td>

DATEPART

</td><td>

sla\_dueDATEPARTMonday@javascript:gs.datePart\('dayofweek','monday','LT'\)

</td><td>

All records in which the date in the **SLA due** field is on a Sunday.

</td></tr><tr><td>

trend \(on\)

</td><td>

\[SLA due\]\[trend\]\[on\]\[Monday\]

</td><td>

DATEPART

</td><td>

sla\_dueDATEPARTMonday@javascript:gs.datePart\('dayofweek','monday','EE'\)

</td><td>

All records in which the date in the **SLA due** field is on a Monday.

</td></tr><tr><td>

relative \(after\)

</td><td>

\[SLA due\]\[relative\]\[after\]\[1\]\[Hours\]\[ago\]

</td><td>

RELATIVEGT

</td><td>

sla\_dueRELATIVEGT@hour@ago@1

</td><td>

All records in which the time on the **SLA due** field is no more than an hour before the time that you entered the query.

</td></tr><tr><td>

relative \(before\)

</td><td>

\[SLA due\]\[relative\]\[before\]\[1\]\[Hours\]\[ago\]

</td><td>

RELATIVELT

</td><td>

sla\_dueRELATIVELT@hour@ago@1

</td><td>

All records in which the time on the **SLA due** field is less than an hour before the time that you entered the query.

</td></tr><tr><td>

is empty

</td><td>

\[SLA due\]\[is empty\]

</td><td>

ISEMPTY

</td><td>

sla\_dueISEMPTY

</td><td>

All records in which the **SLA due** field has no value.

</td></tr><tr><td>

is not empty

</td><td>

\[SLA due\]\[is not empty\]

</td><td>

ISNOTEMPTY

</td><td>

sla\_dueISNOTEMPTY

</td><td>

All records in which the **SLA due** is populated by any value.

</td></tr><tr><td>

is anything

</td><td>

\[SLA due\]\[is anything\]

</td><td>

ANYTHING

</td><td>

sla\_dueANYTHING

</td><td>

All records in which the **SLA due** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[SLA due\]\[is same\] as \[Activity due\]

</td><td>

SAMEAS

</td><td>

sla\_dueSAMEASactivity\_due@day

</td><td>

All records in which there are matching values for the **SLA due** and **Activity due** fields.

</td></tr><tr><td>

is different

</td><td>

\[SLA due\]\[is different\] from \[Activity due\]

</td><td>

NSAMEAS

</td><td>

sla\_dueNSAMEASactivity\_due@day

</td><td>

All records in which there are differing values for the **SLA due** and **Activity due** fields.

</td></tr><tr><td>

is more than

</td><td>

\[SLA due\]\[is more than\]\[1\]\[Days\]\[before\]\[Activity due\]

</td><td>

MORETHAN

</td><td>

sla\_dueMORETHANactivity\_due@day@before@1

</td><td>

All records in which the date value for the **SLA due** field is two or more days previous to the date in the **Activity due** field.

</td></tr><tr><td>

is less than

</td><td>

\[SLA due\]\[is less than\]\[3\]\[Days\]\[before\]\[Activity due\]

</td><td>

LESSTHAN

</td><td>

sla\_dueLESSTHANactivity\_due@day@before@3

</td><td>

All records in which the date value for the **SLA due** field is no more than three days prior to the date in the **Activity due** field.

</td></tr></tbody>
</table>## Operators available for numeric fields

<table id="table_yz1_shy_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

is

</td><td>

\[Reassignment count\]\[is\]\[0\]

</td><td>

=

</td><td>

reassignment\_count=0

</td><td>

All records in which the **Reassignment count** is nothing else but **0**.

</td></tr><tr><td>

is not

</td><td>

\[Reassignment count\]\[is not\]\[0\]

</td><td>

!=

</td><td>

reassignment\_count!=0

</td><td>

All records in which the value for the **Reassignment count** is any number but **0**.

</td></tr><tr><td>

is empty

</td><td>

\[Reassignment count\]\[is empty\]

</td><td>

EMPTY

</td><td>

reassignment\_countISEMPTY

</td><td>

All records in which there is no value in the **Reassignment count** field.

</td></tr><tr><td>

is not empty

</td><td>

\[Reassignment count\]\[is not empty\]

</td><td>

NOTEMPTY

</td><td>

reassignment\_countISNOTEMPTY

</td><td>

All records in which there is any number in the **Reassignment count** field.

</td></tr><tr><td>

less than

</td><td>

\[Reassignment count\]\[less than\]\[2\]

</td><td>

&lt;

</td><td>

reassignment\_count&lt;2

</td><td>

All records in which the value in the **Reassignment count** field is any number less than \(but not equal to\) **2**.

</td></tr><tr><td>

greater than

</td><td>

\[Reassignment count\]\[greater than\]\[2\]

</td><td>

&gt;

</td><td>

reassignment\_count&gt;2

</td><td>

All records in which the value in the **Reassignment count** field is any number greater than \(but not equal to\) **2**.

</td></tr><tr><td>

less than or is

</td><td>

\[Reassignment count\]\[less than or is\]\[2\]

</td><td>

&lt;=

</td><td>

reassignment\_count&lt;=2

</td><td>

All records in which the value in the **Reassignment count** field is one of the following:-   a number less than 2
-   2

</td></tr><tr><td>

greater than or is

</td><td>

\[Reassignment count\]\[greater than or is\]\[2\]

</td><td>

&gt;=

</td><td>

reassignment\_count&gt;=2

</td><td>

All records in which the value in the **Reassignment count** field is one of the following:-   2
-   a number greater than 2

</td></tr><tr><td>

between

</td><td>

\[Reassignment count\]\[between\]\[1\] and \[3\]

</td><td>

BETWEEN

</td><td>

reassignment\_countBETWEEN1@3

</td><td>

All records in which the number in the **Reassignment count** is either 1, 2, or 3.

</td></tr><tr><td>

is anything

</td><td>

\[Reassignment count\]\[is anything\]

</td><td>

ANYTHING

</td><td>

reassignment\_countANYTHING

</td><td>

All records in which the **Reassignment count** field is one of the following:-   any value
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[Reassignment count\]\[is same\] as \[Reopen count\]

</td><td>

SAMEAS

</td><td>

reassignment\_countSAMEASreopen\_count

</td><td>

All records in which there are matching numbers for the **Reassignment count** and **Reopen count** fields.

</td></tr><tr><td>

is different

</td><td>

\[Reassignment count\]\[is different\] from \[Reopen count\]

</td><td>

NSAMEAS

</td><td>

reassignment\_countNSAMEASreopen\_count

</td><td>

All records in which there are differing values between the **Reassignment count** and **Reopen count** fields.

</td></tr><tr><td>

greater than field

</td><td>

\[Reassignment count\]\[greater than field\]\[Reopen count\]

</td><td>

GT\_FIELD

</td><td>

reassignment\_countGT\_FIELDreopen\_count

</td><td>

All records in which the number in the **Reassignment count** field is greater than \(but not equal to\) the number in the **Reopen count** field.

</td></tr><tr><td>

less than field

</td><td>

\[Reassignment count\]\[less than field\]\[Reopen count\]

</td><td>

LT\_FIELD

</td><td>

reassignment\_countLT\_FIELDreopen\_count

</td><td>

All records in which the number in the **Reassignment count** field is less than \(but not equal to\) the number in the **Reopen count** field.

</td></tr><tr><td>

greater than or is field

</td><td>

\[Reassignment count\]\[greater than or is field\]\[Reopen count\]

</td><td>

GT\_OR\_EQUALS\_FIELD

</td><td>

reassignment\_countGT\_OR\_EQUALS\_FIELDreopen\_count

</td><td>

All records in which the number in the **Reassignment count** field is one of the following:-   greater than the number in the **Reopen count** field
-   equal to the number in the **Reopen count** field

</td></tr><tr><td>

less than or is field

</td><td>

\[Reassignment count\]\[less than or is field\]\[Reopen count\]

</td><td>

LT\_OR\_EQUALS\_FIELD

</td><td>

reassignment\_countLT\_OR\_EQUALS\_FIELDreopen\_count

</td><td>

All records in which the number in the **Reassignment count** field is one of the following:-   less than the number in the **Reopen count** field
-   equal to the number in the **Reopen count** field

</td></tr></tbody>
</table>## Operators available for Boolean fields

<table id="table_vfm_d3y_dt"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

is

</td><td>

\[Active\]\[is\]\[true\]

</td><td>

=

</td><td>

active=true

</td><td>

All records in which the **Active** field is **True**.

</td></tr><tr><td>

is not

</td><td>

\[Active\]\[is not\]\[true\]

</td><td>

!=

</td><td>

active!=true

</td><td>

All records in which the **Active** field is **False**, empty, or NULL.

</td></tr><tr><td>

is empty

</td><td>

\[Active\]\[is empty\]

</td><td>

ISEMPTY

</td><td>

activeISEMPTY

</td><td>

All records in which there is no value in the **Active** field.

</td></tr><tr><td>

is not empty

</td><td>

\[Active\]\[is not empty\]

</td><td>

ISNOTEMPTY

</td><td>

activeISNOTEMPTY

</td><td>

All records in which the **Active** field is either **True** or **False**.

</td></tr><tr><td>

is anything

</td><td>

\[Active\]\[is anything\]

</td><td>

ANYTHING

</td><td>

activeANYTHING

</td><td>

All records in which the **Active** field is one of the following:-   True
-   False
-   empty
-   NULL

</td></tr><tr><td>

is same

</td><td>

\[Active\]\[is same\] as \[Made SLA\]

</td><td>

SAMEAS

</td><td>

activeSAMEASmade\_sla

</td><td>

All records in which there are matching values for the **Active** and **Made SLA** fields.

</td></tr><tr><td>

is different

</td><td>

\[Active\]\[is different\] from \[Made SLA\]

</td><td>

NSAMEAS

</td><td>

activeNSAMEASmade\_sla

</td><td>

All records in which there are differing values for the **Active** and **Made SLA** fields.

</td></tr></tbody>
</table>## Operators available for email notifications

|Operator label|Example condition|Equivalent query operator|Example query|Example output|
|--------------|-----------------|-------------------------|-------------|--------------|
|changes|\[State\]\[changes\]|VALCHANGES|stateVALCHANGES|All records in which the **State** field is updated.|
|changes from|\[State\]\[changes from\]\[Awaiting User Info\]|CHANGESFROM|stateCHANGESFROM4|All records in which the **State** field is updated to another value after previously being **Awaiting User Info** \(4\).|
|changes to|\[State\]\[changes to\]\[Awaiting User Info\]|CHANGESTO|stateCHANGESTO4|All records in which the **State** field is updated to **Awaiting User Info** \(4\) after previously being any other value.|

## Operators available for tags

|Operator label|Example condition|Equivalent query operator|Example query|Example output|
|--------------|-----------------|-------------------------|-------------|--------------|
|have|\[Tag\]\[have\]\[Most Active\]|=|sys\_tags.6c361e12471331007f47563dbb9a7135=6c361e12471331007f47563dbb9a7135|All records that have the **Tag** in the value field.|
|does not have|\[Tag\]\[does not have\]\[Most Active\]|DOESNOTHAVE|sys\_tags.6c361e12471331007f47563dbb9a7135DOESNOTHAVE6c361e12471331007f47563dbb9a7135|Any records that has a **Tag** except for the tag mentioned in the value field.|
|excluding|\[Tag\]\[excluding\]\[Most Active\]|EXCLUDING|sys\_tags.6c361e12471331007f47563dbb9a7135EXCLUDING6c361e12471331007f47563dbb9a7135|All records with and without the **Tag** except for the tag mentioned in the value field.|

**Parent Topic:**[Create a condition statement using the condition builder](../task/create-cond-state-using-cond-build.md)

**Related topics**  


[Condition builder](../concept/c_ConditionBuilder.md)

