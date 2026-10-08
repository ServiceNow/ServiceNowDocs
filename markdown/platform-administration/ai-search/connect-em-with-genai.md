---
title: Connect your custom embedding model with Generative AI
description: Integrate a capability definition with your custom embedding model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/connect-em-with-genai.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring an external or custom embedding model, Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Connect your custom embedding model with Generative AI

Integrate a capability definition with your custom embedding model.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_generative_ai_config.list` in the filter to go to the Generative AI Configurations \[sys\_generative\_ai\_config\] table.

2.  Select **New**.

3.  Verify that **Definition Table** field is prepopulated with sys\_one\_extend\_capability\_definition.

4.  In the **Definition** field, select the search icon to select the definition document.

    1.  In the **Table name** field, select One API System Executor \[one\_api\_system\_executor\].

    2.  In the **Document** field, select the OneExtend capability definition that you want to integrate with the embedding model.

    3.  Select **OK**.

5.  In the **Model** field, select an embedding model of your choice.

6.  Select the **Active** option.

7.  Populate the **Additional Configurations** field.

    -   In the **Name** field, enter `resource_path`.
    -   In the **Value** field, enter the end point path of the connection alias URL, the one you created for your embedding model. For example, deployments/text-embedding-3-large/embeddings?api-version=2023-05-15.
8.  Select **Submit**.


