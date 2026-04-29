---
title: Build a needs decision tree
description: Define the decision tree question nodes, decision paths, and guidance for each decision path using Decision Tree Builder.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring needs analysis, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Build a needs decision tree

Define the decision tree question nodes, decision paths, and guidance for each decision path using Decision Tree Builder.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_manager, sn\_prd\_pm.product\_catalog\_admin

## About this task

As you build your decision tree, for example after adding a decision node or a path, you save and close the decision tree record. To continue working on the tree, navigate to the Decision Trees list, select the decision tree record, and open it in Decision Tree Builder, as described in steps 1 through 3 of this procedure.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Needs** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, define the start node:

    1.  Select **New node**

    2.  In the **Node name** field, enter a name for the start node.

    3.  In the **Reference table** field, select the Product Offering Recommendation table.

    4.  Enter the question for the agent to answer.

        You can make the question mandatory by selecting the **Required question** field and enter more details in the **Additional details** field.

    5.  Select the type of answer for your question.

        For a description of the answer types, see [Answer types for questions](https://www.servicenow.com/docs/access?context=type-of-answer&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

    6.  Add more questions.

    7.  Select **Save and close.**

5.  Continue building your decision tree in Decision Tree Builder.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d104962e173">

Option

</th><th align="left" id="d104962e176">

Steps

</th></tr></thead><tbody><tr><td id="d104962e182">

**[Determine the next node displayed in a decision tree](https://www.servicenow.com/docs/access?context=configure-path-in-gdb&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

</td><td>

Configure a path to set the conditions for when the next question is displayed in a decision tree.

</td></tr><tr><td id="d104962e193">

**[Add a follow-up set of questions or instructions in a decision tree](https://www.servicenow.com/docs/access?context=configure-decision-node-in-gdb&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

</td><td>

Configure a question node to add follow-up questions or instructions. An answer to these questions either leads to a guidance or a further set of questions.

</td></tr><tr><td id="d104962e204">

**Add a guidance node for the product recommendation questionnaire**

</td><td>

Configure a guidance node, which identifies the product recommendation displayed after agents answer the questions. The guidance node is the leaf node of a tree.1.  Select the Add path icon on a node.
2.  Select **Add node**.
3.  In the pop-up, select **Propose a guidance as the outcome** and select **Continue**.
4.  Enter a name for the node.
5.  In the **Guidance** field, select Product Offering Recommendation.
6.  In the **Set field inputs to pass data into this guidance** section, select the product recommendation to be displayed.
7.  Select **Save and close**.


</td></tr><tr><td id="d104962e255">

**[Activate a decision tree](https://www.servicenow.com/docs/access?context=activate-guided-decision-tree&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

</td><td>

When your decision tree is complete, select **Activate** in Decision Tree Builder, which validates your tree. If there are no errors, select **Activate now** in the confirmation message dialog box.The decision tree status changes to active.

</td></tr></tbody>
</table>
## What to do next

[Create a needs template and set the catalog relationship](create-publish-needs-template.md).

