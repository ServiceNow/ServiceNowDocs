---
title: Integrate with a custom application or workflow
description: Configure an integration to trigger document task processing or value extraction. Integrations can be used to quickly set up flows with other applications.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Document Intelligence, Enable AI experiences]
---

# Integrate with a custom application or workflow

Configure an integration to trigger document task processing or value extraction. Integrations can be used to quickly set up flows with other applications.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

-   You must first add a target table to your use case before creating an integration.
-   The target table must be readable and writable. Ensure the **Can read** and **Can update** check boxes are selected in the **Application Access** tab of the target table record. For more information, see Create a table.
-   Role required: sn\_docintel.admin or sn\_docintel.manager

## About this task

Define integration points for your Document Intelligence solution. Two integration points are provided for data extraction use cases: one to automatically create and process Document Intelligence document tasks, and one to automatically propagate the field values to another application when extraction has been completed in Document Intelligence. For document classification use cases, there’s also an integration point to map to a data extraction use case.

## Procedure

1.  Do one of the following:

    1.  To integrate a data extraction use case, navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

    2.  To integrate a document classification use case, navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Use Cases**.

2.  Select the use case for which you want to set up integration points.

3.  Do one of the following:

    1.  For a data extraction use case, go to the **Integrations** tab and select **Set up your first integration**.

        If you have already defined one or more integrations and you want to add another, select **New integration**.

        ![New integration button in the Integrations tab of a use case.](../image/integration-setupT3.png)

    2.  For a document classification use case, go to the **Integration Setups** tab and select **New**.

4.  On the form, fill in the fields.

<table id="table_abc_cn4_g5b"><thead><tr><th>

Field for data extraction

</th><th>

Field for document classification

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name your Integration

</td><td>

Name

</td><td>

Name for the integration.

</td></tr><tr><td>

Use case

</td><td>

Use case

</td><td>

Use case to use for the integration task.

</td></tr><tr><td>

Where do you want to take the documents from and store the extracted data?

</td><td>

Target table

</td><td>

Table to receive data from or send data to.

**Note:** The target table is taken from the use case.

</td></tr><tr><td>

What type of integrations you want to set?

</td><td>

Type

</td><td>

For data extraction and document classification use cases, the options include **Process Task** or **Extract Values**. Document classification use cases also have a **Map To Document Data Extraction Use Case** option.

 The **Process Task** type creates an integration point to automatically create and process DocIntel document tasks based on specific triggers happening in the target table.

 The **Extract Values** type creates an integration point to automatically propagate the extracted values to the target table when extraction has been completed in DocIntel \(that is, when the document task status changes to Done\).

 The **Map To Document Data Extraction Use Case** type creates an integration point that allows a processed document classification value to automatically create a new data extraction task.

</td></tr><tr><td>

Conditions

</td><td>

 

</td><td>

Filters used to select certain fields to use as specific triggers for the integration.

 Process Task only.

</td></tr><tr><td>

Create Flow

</td><td>

 

</td><td>

Select this option to create a flow for this integration in Workflow Studio.

 This option should be selected, unless you’re planning to write your own custom script to set up the integration.

</td></tr></tbody>
</table>5.  Do one of the following:

    1.  For data extraction, select **Save**.

    2.  For document classification, select **Submit**.


## Integration

The following images show two example integrations. The first image is a Process Task integration that triggers when a record needs review. The second image is an Extract Values integration that can automatically send extracted fields to the invoice table.

![New integration record with conditions.](../image/configure-integrationT1.png "New Process Task integration")

![New integration record with Extracted Values selected.](../image/integration-setupT2.png "New Extract Values Integration")

## What to do next

If you selected to create a flow, finish the activation in Workflow Studio.

For more information, see Building flows.

**Parent Topic:**[Integrating Document Intelligence with other applications](../concept/integrating-docintel.md)

