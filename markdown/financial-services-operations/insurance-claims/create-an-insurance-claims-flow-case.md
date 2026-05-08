---
title: Initiate an Insurance claims case
description: Initiate an Insurance claims case on behalf of a claimant by using the Insurance claims application. When a customer calls in to report a claim, a claim intake specialist follows this procedure to capture important details and initiate a case.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Initiate an Insurance claims case

Initiate an Insurance claims case on behalf of a claimant by using the Insurance claims application. When a customer calls in to report a claim, a claim intake specialist follows this procedure to capture important details and initiate a case.

## Before you begin

Role required: sn\_ins\_gen\_claim.fnol\_representative

## About this task

This procedure references service definitions and products that are used in the included travel insurance claim line of business. Your workflow may vary depending on your configuration.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select **Report a claim**.

3.  In the Create new case dialog box, select the service definition \(for example, **Report travel claim**\) in the Services list.

4.  Select **Create case**.

5.  In the Select policy activity, search for the client's policy in the **Account** or **Consumer** fields and the **Insurance policy** field.

6.  In the **Incident date** field, enter the date of the incident.

7.  In the **Report date** and **Incident description** fields, add any necessary information.

8.  Confirm that the policy details are correct, and then select **Continue**.

9.  In the Add claim participants activity, add a claim participant by selecting **Add claim participant**.

10. In the Add claim participant form, enter the details of the participant, and then select **Save**.

<table id="choicetable_x5k_v1y_tcc"><thead><tr><th align="left" id="d39665e177">

Reporter status

</th><th align="left" id="d39665e180">

Steps

</th></tr></thead><tbody><tr><td id="d39665e186">

**Is a policy participant**

</td><td>

-   Select the **Select from policy participants** check box.
-   In the **Type** field, select whether the reporter is a person or a company.
-   In the **Consumer** \(person\) or **Account** \(company\) field, use the search function to search for policy participants. The contact details populate after selecting the participant.
-   Enter how the participant is related to the insured in the **Relationship to insured** field.


</td></tr><tr><td id="d39665e225">

**Is not a policy participant**

</td><td>

-   In the **Type** field, select whether the reporter is a person or a company.
-   On the Details form, enter the reporter's details.


</td></tr></tbody>
</table>11. Confirm that all claim participants are added, and then select **Continue**.

12. In the Incident details activity, add an incident that is related to the claim by selecting the add \(![](../../../reuse/icons/product-icons/plus-fill-24.svg)\) icon.

13. For each incident, fill in the incident form with the details of the incident.

    New incidents appear in the incident list for each incident type.

14. If the incident supports itemizing losses and expenses, select the **Itemized loss/expense** tab and create an entry for each one by selecting **New**.

15. Confirm that all incident details are recorded, and then select **Continue**.

16. In the Upload documents activity, upload any supporting documentation that was provided by the claimant.

17. Confirm that all required documents are uploaded, and then select **Continue**.

18. In the Submit claim activity, enter any additional comments, and then select **Submit**.


## Result

A claim case is created in the New state and the workflow is triggered. The cases are assigned to an assignment group that is based on the defined assignment rules.

## What to do next

Processors and adjusters assign cases to themselves and start working on them. For more information, see [Process an Insurance claims case](process-an-insurance-claims-flow-case.md) and [Work on Insurance claims adjuster tasks](manage-an-insurance-claims-flow-case.md).

