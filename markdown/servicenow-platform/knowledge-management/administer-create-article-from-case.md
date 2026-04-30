---
title: Enable creating an article from a customer service case
description: You can enable authors to reuse information in a case by copying case details into an article template. Use the pre-defined customer service source case table to article template target table configuration or create custom configurations between the two tables to copy information from a case to an article.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable creating an article from a customer service case

You can enable authors to reuse information in a case by copying case details into an article template. Use the pre-defined customer service source case table to article template target table configuration or create custom configurations between the two tables to copy information from a case to an article.

## Before you begin

-   The [Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md) must be active.
-   The [Properties installed with Customer Service Management](https://www.servicenow.com/docs/access?context=r_PropInstallWcustServ&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) must be enabled
-   The pre-defined KCS article template or a newly created article template must be active.

    **Note:** You can do one of the following to create an article from a case:

    -   Use the pre-defined **Case KCS Article** mapping as is or modify the field mappings between the case source table and article template target table.
    -   Create a new article template target table and map it to the case source table and customize the field mappings between them. For information on creating article templates, refer to [Create an article template](../task/create-a-new-article-templates.md).
-   Knowledge users use the **Create Knowledge** button in a case form to create an article from a case and must have "can contribute" permission for at least one active knowledge base to create an article from a case. For information on user permissions, see [Knowledge Management roles](../reference/r_KnowledgeRoles.md#).

Role required: sn\_customerservice.customer\_admin or admin

## About this task

The pre-defined **Case KCS Article** mapping is stored in the CSM Table Map \[csm\_table\_map\] table. This configuration has the sn\_customerservice\_case source case table configured to the kb\_template\_kcs\_article target article template table with the four field mappings pre-configured between the tables. You can customize the existing field mappings or map additional fields between the tables.

## Procedure

1.  In the application filter navigator, type `csm_table_map.list`.

2.  Click **Case KCS Article**.

3.  From the **Target Table** list, use the pre-defined KCS article template table or select the newly created article template table.

4.  Map each customer service case field that must be used to create knowledge articles.

    1.  In the **Basic Field Mapping** related list, click **New**.

        To map fields, fill in the following fields:

        |Field|Instructions|
        |-----|------------|
        |Source Field|Select the field in the source case table that contains the information to be copied to the field in the article template target table.|
        |Target Field|Select the field in the article template target table to which you need information copied to from the field in the source case table.|

    2.  Click **Submit**.

    3.  To map fields using advanced scripts, select the **Advanced Field Mapping** check box and then map the fields between the source and the target table using advanced scripts in the **Advanced Field Mapping** tab.

        **Note:**

        If the same source or target field is configured in both the basic and advanced field mappings, the advanced field mapping overrides the basic field mapping.

        If the fields configured in the basic and advanced field mapping are different, the field configurations in the advanced field mapping are appended to the field configurations in the basic field mapping.

    4.  To customize when and how the **Create Knowledge** button is displayed, use the condition builder in the **Condition** tab or select **Use Advanced Condition** check box and configure using advanced scripts.

        **Note:** If you change the target table in the **Case KCS Article** mapping, also update the scripts with the configuration changes for display of this button.

5.  Click **Update**.


