---
title: View normalization suggestions in Software Asset Management classic
description: View normalization suggestion records that are created for discovery models. You can accept or reject these suggestions.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# View normalization suggestions in Software Asset Management classic

View normalization suggestion records that are created for discovery models. You can accept or reject these suggestions.

## Before you begin

Role required:

-   sam\_admin: accepts or rejects the normalization suggestions.
-   sam\_user: views normalization suggestions.

The records are contained in the Normalization Suggestions \[samp\_normalization\_suggestions\] table.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Normalization Suggestions** For details on the normalization suggestion fields, see [Normalization suggestions for discovery models](../concept/normalization-suggestions.md).

    **Note:** Suggested field values that differ from actual field values are indicated by a blue dot.

2.  Select **Accept** to make the suggested changes to the discovery model, or click **Reject** to keep the existing settings.

    **Note:** Only the sam\_admin role can accept or reject the normalization suggestions. For more details on accepting or rejecting suggestions, see [Normalization suggestions for discovery models](../concept/normalization-suggestions.md).


-   **[View a software job result](t_ViewAJobResult.md)**  
You can view the results of Software Asset Management jobs that have run to verify completion.
-   **[Manually normalize a software discovery model in Software Asset Management classic](t_EditASoftwareDiscModel.md)**  
You can edit a software discovery model to manually normalize discovered software that has not been fully normalized \(partially normalized, publisher normalized, or match not found\) on the Software Discovery Models form so that it can be reconciled.
-   **[Manually override edition value in Software Asset Management classic](t_ManOverrideEdition.md)**  
When the edition of a software install is not automatically discovered, you can specify the edition on the Software Installation form with the correct value \(if known\) so the software can be successfully reconciled.
-   **[Discovered engineering licenses in Software Asset Management classic](../concept/discovered-eng-licenses.md)**  
View a list of all the discovered and normalized software for your engineering applications.

**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

