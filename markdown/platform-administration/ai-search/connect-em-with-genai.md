---
title: Connect your custom embedding model with the Generative AI application
description: Integrate your custom embedding model with a capability definition to help the Generative AI application understand your data better and deliver more relevant, tailored responses.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Connect your custom embedding model with the Generative AI application

Integrate your custom embedding model with a capability definition to help the Generative AI application understand your data better and deliver more relevant, tailored responses.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_generative_ai_config.list` in the filter to go to the Generative AI Configurations \[sys\_generative\_ai\_config\] table.

2.  Select **New**.

3.  Ensure that **Definition Table** field is prepopulated with sys\_one\_extend\_capability\_definition.

4.  In the **Definition** field, select the search icon \(![Lookup documents using list.](../../../common/image/Banner_GlobalTextSearchIcon.png)\)to select the definition document.

    1.  In the **Table name** field, select One API System Executor \[one\_api\_system\_executor\].

    2.  In the **Document** field, select the OneExtend capability definition that you want to integrate with the embedding model.

    3.  Select **OK**.

5.  In the **Model** field, select an embedding model of your choice.

6.  Select the **Active** option.

7.  Populate the **Additional Configurations** field.

    -   In the **Name** field, enter `resource _path`.
    -   In the **Value** field, enter the end point path for the connection alias URL that you created for your embedding model.

        For example, `/text-embedding-3-large/embeddings?api-version=2023-05-15`.

8.  Select **Submit**.


**Parent Topic:**[Configuring bring your own model \(BYOM\)](../concept/creating-byom.md)

