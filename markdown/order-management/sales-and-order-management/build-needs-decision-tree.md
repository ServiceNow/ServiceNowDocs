---
title: Build a needs decision tree
description: Define the decision tree question nodes, decision paths, and guidance for each decision path using Decision Tree Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/order-management/sales-and-order-management/build-needs-decision-tree.html
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring needs analysis, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Build a needs decision tree

Define the decision tree question nodes, decision paths, and guidance for each decision path using Decision Tree Builder.

## Before you begin

Role required: sn\_prd\_pm.product-catalog\_manager, sn\_prd\_pm.product-catalog\_admin

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

        For a description of the answer types, see [Answer types for questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/type-of-answer.md).

    6.  Add more questions.

    7.  Select **Save and close.**

5.  Continue building your decision tree in Decision Tree Builder.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d30596e173">

Option

</th><th align="left" id="d30596e176">

Steps

</th></tr></thead><tbody><tr><td id="d30596e182">

**[Determine the next node displayed in a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/configure-path-in-gdb.md)**

</td><td>

Configure a path to set the conditions for when the next question is displayed in a decision tree.

</td></tr><tr><td id="d30596e193">

**[Add a follow-up set of questions or instructions in a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/configure-decision-node-in-gdb.md)**

</td><td>

Configure a question node to add follow-up questions or instructions. An answer to these questions either leads to a guidance or a further set of questions.

</td></tr><tr><td id="d30596e204">

**[Provide actions to agents in a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/configure-guidance-in-gdb.md)**

</td><td>

Configure a guidance node so agents can view the product recommendation after completing the questionnaire.

</td></tr><tr><td id="d30596e215">

**[Activate a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/activate-guided-decision-tree.md)**

</td><td>

When your decision tree is complete, select **Activate** in Decision Tree Builder, which validates your tree. If there are no errors, select **Activate now** in the confirmation message dialog box.The decision tree status changes to active.

</td></tr></tbody>
</table>
## What to do next

[Create a needs template and set the catalog relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/order-management/sales-and-order-management/create-publish-needs-template.md).

