---
title: Create an insurance product model
description: Create an insurance product model for an insurance policy that is sold to a customer by using the Insurance claims application. The insurance product model defines the product type, which customers that the policy is for, and the coverage specifications.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Insurance product models, Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an insurance product model

Create an insurance product model for an insurance policy that is sold to a customer by using the Insurance claims application. The insurance product model defines the product type, which customers that the policy is for, and the coverage specifications.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the Label column, search for either the personal insurance model or the commercial insurance model.

<table id="choicetable_hsn_gnv_2dc"><tbody><tr><td id="d85068e79">

**Personal insurance model**

</td><td>

Search for and select **Personal lines insurance product model**.

</td></tr><tr><td id="d85068e91">

**Commercial insurance model**

</td><td>

Search for and select **Commercial lines insurance product model**.

</td></tr></tbody>
</table>3.  On the **Columns** tab, in the Label column, search for and select **Service Type**.

4.  Set the application scope in your instance to **Expanded Model and Asset Classes**.

5.  On the **Choices** tab, select **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table|Table for either a personal insurance model or a commercial insurance model. You can select **personal insurance model** for a personal lines insurance product or **commercial insurance model** for a commercial lines insurance product,|
    |Label|Display name of the product insurance model.|
    |Value|Name of the product insurance model in snake case.|

7.  Select one of the following insurance models to navigate to.

    |Insurance model|Navigation|
    |---------------|----------|
    |**Personal insurance model**|Navigate to **All** &gt; **Financial Services Operations** &gt; **Products** &gt; **Personal Insurance Models**.|
    |**Commercial insurance model**|Navigate to **All** &gt; **Financial Services Operations** &gt; **Products** &gt; **Commercial Insurance Models**.|

8.  Select **New**.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the insurance product model.|
    |Product code|Unique identification code for this insurance product.|
    |Product type|Insurance product type that you created earlier in this procedure.|
    |Specification|Coverage Specification. For more information, see [Coverage specification](../concept/coverage-specification.md).|
    |Short description|Brief description of this product model.|

10. Select **Submit**.


