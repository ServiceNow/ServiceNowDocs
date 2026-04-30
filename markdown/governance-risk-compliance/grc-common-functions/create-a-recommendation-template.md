---
title: Create a recommendation template
description: Create a recommendation template to train the AI models with a data set for identifying your key business operations. Key business operations include managing regulatory changes, assessing risks, and adhering to compliance guidelines.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Recommendation contexts and templates, Common GRC features, Governance, Risk, and Compliance]
---

# Create a recommendation template

Create a recommendation template to train the AI models with a data set for identifying your key business operations. Key business operations include managing regulatory changes, assessing risks, and adhering to compliance guidelines.

## Before you begin

Create a recommendation context before you create a recommendation template. For more information, see [Recommendation contexts and templates](../concept/recommendation-contexts.md).

Role required: sn\_reco\_template.recommendation\_config\_writer or sn\_reco\_template.recommendation\_writer

## Procedure

1.  Navigate to **All** &gt; **GRC Administration** &gt; **Recommendation contexts**.

2.  Select the recommendation context that you want to add the recommendation templates to.

    1.  In the Recommendation templates related list, select **New**.

    2.  From the Recommended item drop-down list, select an item.

        The recommended item that you select appears as the Recommendation template in the Recommendation templates related list.

        For example, let's say that you want to create a template for suggesting the remediation tasks for an issue. In this case, select **remediation task** as the recommended item.

        ![Recommendation templates related list.](../image/reco-templates.png)

    3.  In the **Extension point** field, enter an extension point.

    4.  In the **Display order** field, enter the order that you want the extension points to be displayed.

    5.  If you want the recommendation template to be active, select the **Active** check box.

    6.  If you want the recommendation template to display the **Relationship section** tab, select the **Show relationships** check box.

3.  On the **Advanced AI-search** tab, enter the required inputs.

    1.  In the Advanced AI-search drop-down list, select either the **Predictive intelligence** option or the **GenAI** option.

        Select the AI search type that best matches your needs for recommending the relevant items that are based on the context and criteria.

        -   If you select **Predictive intelligence**, you must select an AI model.
        -   If you select **GenAI**, you must select the skill.
4.  On the **Relationship section** tab, enter **Heading** and **Sub heading**.

    The Heading and Sub heading appear on the Relationships section in the Workspace view of a record.

    For example, you can [fetch recommendations](../../now-assist-irm/task/create-recommendation-reg-alert.md) for remediation tasks for an issue by using the Now Assist for IRM application.

5.  On the form header, select **Save**.

6.  From the Recommendation templates related list, select a recommendation template.

7.  From the Card details related list, select **New**.

    1.  From the Field drop-down list, select a value.

        Each field that you select appears as a field with its value on the recommendation card.

    2.  In the **Display order** field, enter a value for the order that you want the recommendation template to be displayed.

    3.  If you want the **Key** field to appear on the recommendation card, select **Active**.

    4.  Repeat steps a to c for all the fields that you want to appear on the recommendation card in the Workspace view.

8.  From the Sub header details related list, select **New**.

    1.  From the Field drop-down list, select a value.

        Each field that you select appears as a field with its value on the recommendation card.

    2.  In the **Display order** field, enter a value for the order that you want the recommendation template to be displayed.

    3.  If you want the **Key** field to appear on the recommendation card, select the **Active** check box.

    4.  Repeat steps a to c for all the fields that you want to appear on the recommendation card in the Workspace view.

9.  From the Details related list, select **New**.

    1.  From the Field drop-down list, select a value.

        Each field that you select appears as a field with its value on the recommendation card.

    2.  In the **Display order** field, enter a value for the order that you want the recommendation template to be displayed.

    3.  If you want the **Key** field to appear on the recommendation card, select the **Active** check box.

    4.  Repeat steps a to c for all the fields that you want to appear on the recommendation card in the Workspace view.

10. From the Relationships registry related list, select **New**.

    Identify the dependent record type that you need to achieve the intended results for the scoped recommendation record type.

    A relationship registry shows the relationship between a record and the objects that are defined in a table. You can configure the details, such as the name, source, table name, or filter conditions.

    Each entry that you add appears as a column on the child relationships section of the recommendation in the Workspace view.

    1.  On the **Relationships registry** tab, select **New**.

    2.  In the **Relationship registry** field, search and select a record.

        The record that you select appears in the Relationship table field as a read-only value. For example, if you select **Child Control Objectives**, you can see the **\[sn\_compliance\_policy\_statement\]** in the relationship table field.

    3.  In the **Conditions** field, add the conditions for your requirement.

    4.  In the **Display order** field, enter a value.

    5.  If you want the **Registry details** to be active, select the **Active** check box.

    6.  Select **Submit**.

11. Select **Update**.


## Result

A recommendation template is configured for the selected recommendation context.

**Parent Topic:**[Recommendation contexts and templates](../concept/recommendation-contexts.md)

