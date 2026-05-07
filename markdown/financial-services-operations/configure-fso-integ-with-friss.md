---
title: Configure Financial Services Operations Integration with FRISS
description: Select and configure the Financial Services Operations Integration with FRISS subflows to obtain the fraud score for your organization.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [FRISS, Integrate, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Operations Integration with FRISS

Select and configure the Financial Services Operations Integration with FRISS subflows to obtain the fraud score for your organization.

## Before you begin

Role required: admin

## About this task

In this procedure, you can select either the **Look up Claim Fraud Score via Spoke selector** or **Look up Claim Fraud Score** subflow option.

**Tip:** The **Look up Claim Fraud Score via Spoke selector** option requires minimal configuration and enables you to configure multiple third-party adapter systems.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Subflows** tab.

3.  Depending on which subflow option you select, complete the following actions.

<table id="choicetable_ldc_fz3_zwb"><thead><tr><th align="left" id="d120941e108">

Option

</th><th align="left" id="d120941e111">

Description

</th></tr></thead><tbody><tr><td id="d120941e117">

**Look up Claim Fraud Score**

</td><td>

1.  In the **Application** search field, search for Financial Services Operations Integration with FRISS.
2.  From the list of saved subflows, look for the **Look up Claim Fraud Score** option and open it.


</td></tr><tr><td id="d120941e144">

**Look up Claim Fraud Score via Spoke selector**

</td><td>

1.  In the **Application** search field, search for **Financial Services Operations Core**.
2.  In the Name **Search** field, search for the **Look up Claim Fraud Score via Spoke selector** option and open it.


</td></tr></tbody>
</table>4.  Select **Test**.

    The Test Subflow dialog opens.

    Define the input values for the subflow to use in its actions. The values that you define are automatically filled in on future test runs.

5.  Select **Run Test**.

    **Note:** Select the **Run test in background** option to test a subflow asynchronously in the background. If you select the option, the execution details are displayed only after the execution completes asynchronously in the background. Also, the execution details are associated with the subflow only after execution completes.

6.  After the flow executes, select **Subflow has been executed. To view the subflow, click here**.

    The Execution Details open.


**Parent Topic:**[Financial Services Operations Integration with FRISS](../concept/fso-integration-with-friss-overview.md)

