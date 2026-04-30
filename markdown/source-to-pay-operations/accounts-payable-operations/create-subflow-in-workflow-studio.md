---
title: Create subflow in workflow studio
description: Use subflows to configure conditions that are applied on the invoice and raise an exception.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create an invoice exception definition, Invoice exceptions, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Create subflow in workflow studio

Use subflows to configure conditions that are applied on the invoice and raise an exception.

## Before you begin

Role required: admin

This video shows you how to create subflow in workflow studio.The video shows you how to create subflows in workflow studio. 

## Procedure

1.  Navigate to **Workflow Studio** &gt; **New** &gt; **Subflows**.

    The subflow page appears.

2.  Enter the **Subflow name**.

3.  Enter the **Description**.

4.  Choose the **Application** as Accounts Payable Invoice Processing in the drop-down list.

5.  Click **Build subflow**.

6.  Configure Inputs and Outputs for Subflow.

    Example: In Subflows, you must fetch the invoice record based on sys\_id. Traverse through the invoice record and check if the condition business owner or legal entity is empty. If the condition matches, then the system raises an exception.

    1.  In the **Inputs** area, enter **Label** as invoice Sysids.

    2.  Enter **Name** as invoice\_sysids.

    3.  The **Type** drop-down is auto-populated with String.

    4.  Select **Done**.

    5.  In the header area, click **Flow variables**.

        The Flow variables pop-up appears.

    6.  Enter **Label** as Condition result.

    7.  Enter **Name** as Condition result.

    8.  Choose **Type** as True/False.

    9.  Select **Save**.

7.  In **Actions** area, perform the following steps:

    1.  Select **Action** as **Look Up Records** from the drop-down list.

    2.  In the **Table** field, search for**invoice \[sn\_shop\_invoice\]**.

    3.  Configure the **Conditions** as **sys\_id is one of invoice SysIDs**.

    4.  In **Actions** &gt; Accounts Payable Invoice Processing &gt; Look Up Records.

    5.  Select **Table** as Invoice \[sn\_shop\_invoice\]

    6.  Set the **Conditions** &gt; **SysID** &gt; **is one of** &gt; **Subflows- Inputs** &gt; **invoice Sysids**.

    7.  Select **Done**.

    8.  Create **Flow logic** &gt; **For Each item in** &gt; **Look Up Records** &gt; **Invoice Records &gt; Done**.

    9.  Select **If** &gt; **Condition1** &gt; **For Each** &gt; **Invoice Record** &gt; **Business owner** &gt; **is empty**.

    10. Select **If** &gt; **Condition2** &gt; **For Each** &gt; **Invoice Record** &gt; **Legal entity** &gt; **is empty**.

    11. Select **then** &gt; ![](../image/plus-icon.png) icon.

    12. Click **Done**.

    13. Add a flow logic as **Set Flow variable**.

    14. Choose **Condition result** from the drop-down list.

    15. Select the **Data** check-box.

    16. Select **Done**.

    17. Add a **Flow logic** as **Set Flow variables**.

    18. Choose **Condition result** from the drop-down list.

    19. Select **Done**.

    20. Select **Save**.

    21. Choose **Action** &gt; **Accounts Payable Invoice Processing** &gt; **Generate Exception and Line Exceptions** from the drop-down list.

    22. Choose **Condition result** as **Flow Variable**.

    23. Choose **Exception Definition Record** as Missing BO or LegalEntity.

    24. Choose the **Invoice** as For Each &gt; Invoice record.

    25. Enter the description.

    26. Select **Done**.

    27. Select **Save**.

        Success message appears as the subflow is saved successfully.

8.  Select **Publish**.

    You are prompted with an alert message "Are you sure you want to publish this subflow? Your changes will be applied to all instances where this subflow is being used."


## Result

The subflow is successfully created.

**Parent Topic:**[Create an invoice exception definition](define-new-invoice-exception.md)

