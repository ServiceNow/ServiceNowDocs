---
title: Explain the risk of a change request by using Now Assist for IT Service Management \(ITSM\)
description: Quickly generate the explanation of the calculated risk rating for a change request by using the change request risk explanation skill in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Explain the risk of a change request by using Now Assist for IT Service Management \(ITSM\)

Quickly generate the explanation of the calculated risk rating for a change request by using the change request risk explanation skill in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

Role required: itil

## About this task

Data from these input fields in the change request input table is used to explain why a change risk is rated high, medium, or low:

-   Short description
-   Implementation plan
-   Assignment group
-   Risk
-   Description
-   Backout plan
-   Model type

Additional inputs include:

-   Similar change requests and the incidents caused by those changes
-   Risk condition that was met
-   Risk assessment

    By default, the assessment uses the top five normalized risk values sorted in descending order. If there’s a tie between the two values, the one with the lower order number is used. For information on risk assessment, see [Risk assessment](../../change-management/concept/c_RskAsmtCalc.md).


You can also add custom input fields.

You can generate the explanation of the calculated risk rating for a change request in Core UI and Service Operations Workspace for ITSM.

## Procedure

1.  In Core UI or Service Operations Workspace for ITSM, open a change request that is assigned to you.

2.  Select the Now Assist icon ![Now assist icon.](../../../common/image/icon-ai-sparkle.png) for the **Explain Risk** field.

    **Note:** The Now Assist icon ![Now assist icon.](../../../common/image/icon-ai-sparkle.png) isn’t available if the risk for the change request hasn’t already been calculated.

    The risk explained by Now Assist appears in a window on the change request record.

    ![The Change Risk explanation includes a list of relevant change requests to help you understand which risk factors contributed to the calculated risk](../image/now-assist-itsm-change-risk-citation.png)

3.  Elaborate or shorten the risk explained by Now Assist.

    -   To lengthen the generated response, select **Refine** &gt; **Elaborate**.
    -   To shorten the generated response, select **Refine** &gt; **Shorten**.
4.  When you're finished generating the explanation for a change request risk rating, you can provide feedback, copy it, or view information about it.

<table id="choicetable_c2n_fsz_xbc"><thead><tr><th align="left" id="d262005e245">

Option

</th><th align="left" id="d262005e248">

Procedure

</th></tr></thead><tbody><tr><td id="d262005e254">

**Provide feedback for the change request risk explanation**

</td><td>

If you think that the change request risk explanation was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the change request risk explanation wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d262005e277">

**Copy the change request risk explanation**

</td><td>

If you want to reuse the change request risk explanation, select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\).

</td></tr><tr><td id="d262005e292">

**View the information about the change request risk explanation**

</td><td>

If you want to check some details about the change request risk explanation, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
