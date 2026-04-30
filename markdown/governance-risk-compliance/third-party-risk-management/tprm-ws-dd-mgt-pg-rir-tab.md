---
title: Risk intelligence report requests management
description: You can view a list of risk intelligence report \(RIR\) requests, their associated providers, scores, and report URLs. In addition, you can create requests and make updates by using the Third-party Risk Management application.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Risk intelligence report requests management

You can view a list of risk intelligence report \(RIR\) requests, their associated providers, scores, and report URLs. In addition, you can create requests and make updates by using the Third-party Risk Management application.

## Risk intelligence report request process

If you have the third-party risk \(TPR\) assessor \[sn\_vdr\_risk\_asmt.vendor\_risk\_assessor\] or TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can request a RIR or score. You can create a RIR request that is associated with a third party or due diligence request. If you want to associate an RIR request with a due diligence request, it must be after an inherent risk questionnaire \(IRQ\) has been completed \(that is when the due diligence request has entered the IRQ in progress state\). You can update the Sanction section at any time.

For more information, see [Request a risk intelligence report](../../grc-vendor-risk/task/tprm-riskintel-request-tp.md), [Request a risk intelligence report associated with a due diligence request](../../grc-vendor-risk/task/tprm-riskintel-request-dd.md), [Risk intelligence report request form](tprm-rir-form.md), and [Track sanctions-related information](../../grc-vendor-risk/task/tprm-riskintel-track-sanctions.md).

The following example shows how a new risk intelligence report request appears in Vendor Management Workspace.

![Risk intelligence report request view from the Details tab on the report request page.](../../grc-vendor-risk/image/tprm-ws-rir.png "Example of a risk intelligence report request")

The following table shows the information that is captured in an RIR request.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Risk intelligence report request section**

</td></tr><tr><td>

Number

</td><td>

Unique ID number that is auto-assigned by the system and starts with the text RIR.

</td></tr><tr><td>

Provider

</td><td>

Organization that is responsible for generating the risk intelligence information for the request.

</td></tr><tr><td>

Request type

</td><td>

Type of report or score that is provided.

 Each service that is offered by the provider returns a particular type of risk rating or score. For example, Financial risk or Security risk.

**Note:** The request types that are available are dependent on what has been set up for the provider. For more information, see [Set up a request type for a provider](../../grc-vendor-risk/task/tprm-riskintelprvdr-request-type.md).

</td></tr><tr><td>

Third party

</td><td>

Third party that is to be scored by the provider.

</td></tr><tr><td>

Due diligence request

</td><td>

Due diligence request that is associated with the risk intelligence request. There’s an option to request risk intelligence as part of a due diligence request.

For more information, see [Request a risk intelligence report associated with a due diligence request](../../grc-vendor-risk/task/tprm-riskintel-request-dd.md).

</td></tr><tr><td>

Short description/Description

</td><td>

Text that explains and clarifies the intent of the request for stakeholders.

</td></tr><tr><td>

State

</td><td>

Current state of the request:

-   Open
-   Order pending
-   Order in progress
-   Closed complete
-   Closed incomplete

</td></tr><tr><td>

Request date

</td><td>

Date that the order is pending and ready to be sent to the provider.

</td></tr><tr><td>

Received date

</td><td>

Date that the response from the provider is received.

</td></tr><tr><td class="sub-head" colspan="2">

**Report results section**

</td></tr><tr><td>

Score

</td><td>

Overall risk score that is determined by the provider.

</td></tr><tr><td>

URL

</td><td>

Link to additional information about the origin of the generated score.

</td></tr><tr><td>

Score generated on

</td><td>

Date that the score is generated.

</td></tr><tr><td class="sub-head" colspan="2">

**Sanction section**

</td></tr><tr><td>

Sanctioned

</td><td>

Option that you can select **Yes** to indicate that the third party is sanctioned. This field is set to **No** by default.

</td></tr><tr><td>

Start date

</td><td>

Start date of the sanctioned enforcement.

</td></tr><tr><td>

End date

</td><td>

End date of the sanctioned enforcement.

</td></tr><tr><td>

Details

</td><td>

Text that explains and clarifies the type of sanction and how it impacts your business relationship with the third party.

</td></tr></tbody>
</table>## Risk intelligence report requests tab

While viewing the data for a third party, you can select the **Risk intelligence report requests** tab to view the list of report requests.

The following example shows the **Risk intelligence report requests** tab in Vendor Management Workspace.

![Risk intelligence report requests view from Risk intelligence Report requests tab in Vendor Management Workspace.](../../grc-vendor-risk/image/tprm-ws-rir-tab.png "Risk intelligence report requests tab")

For more information on RIR requests, see [Using risk intelligence reports and scores](../../grc-vendor-risk/concept/tprm-riskintel-using.md).

## Risk intelligence report request states

The RIR requests have the following potential states:

-   **Open**

    An RIR request enters this state after the record has been created and saved by the Third-party Risk \(TPR\) manager, TPR assessor, or contract negotiator that is assigned to the due diligence request. For each risk intelligence request, the system auto-assigns a unique ID number that starts with the text RIR.

-   **Order pending**

    An RIR request enters this state after the record has been reviewed and submitted by the Third-party Risk \(TPR\) manager, TPR assessor, or contract negotiator that is assigned to the due diligence request.

    The following changes take place:

    -   The order has been submitted to the provider.
    -   The **Request date** field has been populated with the date that this record was submitted on.
    -   All fields in the Risk intelligence report request section are read-only.
-   **Order in progress**

    An RIR request enters this state after the order has been received by the provider.

    The following changes take place:

    -   The score records are generated with the report request.
    -   The **Score generated on** field is updated.
-   **Closed incomplete**

    An RIR request enters this state after the order was received by the provider but couldn’t be processed due to an error, and the order was closed.

-   **Closed complete**

    An RIR request enters this state after the order was received and processed by the provider.

-   **Canceled**

    An RIR request enters this state after a TPR manager, TPR assessor, or contract negotiator cancels the report request. If you must cancel a request, it can be done while the request is in the **Open** or **Order pending** state. If you want to create a duplicate of a canceled request, you can’t edit that record. You must create a new RIR request.


-   **[Risk intelligence report request form](tprm-rir-form.md)**  
Use the risk intelligence request form to capture all the information that you need to request risk intelligence using Third-party Risk Management. As a third-party risk manager, third-party risk assessor, and contract negotiator that is assigned to the due diligence request, you can request risk intelligence.

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Integrating scores from risk intelligence providers](../../grc-vendor-risk/concept/tprm-riskintelprvdr-overview.md)

[Risk intelligence report request form](tprm-rir-form.md)

[Risk intelligence provider integrations](../../grc-vendor-risk/concept/tprm-integrate-rir.md)

[Integrating EcoVadis with Third-party Risk Management](../../grc-vendor-risk/concept/tprm-integrating-ecovadis.md)

