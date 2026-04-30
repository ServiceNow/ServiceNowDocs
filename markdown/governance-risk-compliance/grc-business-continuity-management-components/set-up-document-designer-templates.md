---
title: Set up the template configurations
description: Set up the template relationship registry using the Template Configurations module from the General administration setup. Configure data relationships, content configurations, and scripted variables for using the Document designer application so that required data gets displayed in the reports.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Generating reports using Document designer, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up the template configurations

Set up the template relationship registry using the Template Configurations module from the General administration setup. Configure data relationships, content configurations, and scripted variables for using the Document designer application so that required data gets displayed in the reports.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Template Configurations**.

2.  In the Template Configurations module, select **New** to create a template.

    Instead of using the predefined templates, you can create templates in the Template Configurations module.

    The predefined Microsoft Word templates that are available with the base version are displayed in the Template Configurations module. The example shows the BIA template, BCP template, and Events template.

    ![Template configurations.](../image/temp-config-module.png)

    The example shows how to create a template configuration in your instance.

    ![New template configuration form.](../image/new-template-config.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the template configuration. For example, you can specify `BIA template configuration` or `BCP template configuration`.|
    |Table|Table on which the report is generated.|
    |Fields|Fields from which data must be displayed on the report. Move the required fields from the **Available** list to the **Selected** list.|
    |Business domain|Domain from which the template is being configured. In this example, it is set to **BCM**.|

    The example shows the template configuration for the "BCP template."

    ![BCP template configuration.](../image/data-rela-template-config.png)

4.  Select **Submit**.

5.  To edit an existing template, select the template from the list and edit the data relationships, content configurations, and scripted variables.

    You can update the data relationships, content configurations, and scripted variables for the predefined template.

6.  Select **Update**.


## What to do next

For the newly created template, create a data relationship path from the template configuration to navigate to any table that you require. For more information, see [Configure the data relationships](create-data-rel-fortemp-config.md).

