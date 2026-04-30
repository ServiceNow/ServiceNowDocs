---
title: Viewing and updating Governance, Risk, and Compliance exceptions
description: Report exceptions as it is critical for businesses to quickly identify and address key business process issues before they become a problem. Using exceptions to manage errors has advantages over traditional error-management techniques.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Viewing and updating Governance, Risk, and Compliance exceptions

Report exceptions as it is critical for businesses to quickly identify and address key business process issues before they become a problem. Using exceptions to manage errors has advantages over traditional error-management techniques.

## Before you begin

Role required: sn\_grc.admin

## About this task

An exception report is a document that lists instances in which actual performance is deviated from expectations. GRC exception is a capability using which you can record or associate business exceptions with GRC objects such as citations, automated factors, and so on. Each exception record has details such as the category of the exception, the record in the table, and the field with which the exception is associated. The administrator can view the list of exceptions and resolve them. Whenever an exception is raised, the solution to resolve the exception is also given in the exception description. The administrator uses the proposed solution to resolve the exception. An example of an exception is when a user has not configured a risk assessment methodology but is trying to perform an object assessment. When an administrator resolves one type of exception, all other similar exceptions get resolved.

## Procedure

1.  Navigate to **GRC Exceptions** &gt; **Exception Report**.

2.  Open the exception record you want to resolve.

3.  On the form, fill in the field.

<table id="table_p33_rrc_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the exception that is raised.

</td></tr><tr><td>

Exception category

</td><td>

Category to which an exception belongs. The choices are:-   Configuration: Example: A risk administrator tries configuring a form and giving a user the authority to perform a task for which the user does not have the right role.
-   Runtime: Example: When something runs automatically such as an Indicator.


</td></tr><tr><td>

State

</td><td>

State of exception. The default state is **Open**.

</td></tr><tr><td>

Application

</td><td>

Application to which the exception belongs.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the exception and the possible solution for resolution.

</td></tr><tr><td class="sub-head" colspan="2">

Exception Record Details

</td></tr><tr><td>

Source table

</td><td>

Table on which the exception has occurred.

</td></tr><tr><td>

Record reference

</td><td>

Record on which the exception has occurred. For example, an exception is raised on a risk assessment instance response.

</td></tr><tr><td>

Column reference

</td><td>

The column that contains the record.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Notes on the resolution of the exception or any other additional information.

</td></tr><tr><td>

Activities

</td><td>

Displays the stream of activities on the exception.

</td></tr></tbody>
</table>4.  Click **Update** after you change the state of the exception.

5.  Click **Delete** to delete the record.


**Parent Topic:**[Common Governance, Risk, and Compliance features](../../grc-common/concept/common-grc-features.md)

