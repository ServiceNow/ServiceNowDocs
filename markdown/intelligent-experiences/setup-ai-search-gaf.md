---
title: Set up AI Search for GAF
description: Configure AI Search to enable Group Action Framework \(GAF\) to improve quality and consistency of agentic AI and Now Assist generative AI on the Now Platform.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [gaf]
breadcrumb: [GAF, Configure, Now Assist AI agents, Enable AI experiences]
---

# Set up AI Search for GAF

Configure AI Search to enable Group Action Framework \(GAF\) to improve quality and consistency of agentic AI and Now Assist generative AI on the Now Platform.

## Before you begin

Role required: admin

## About this task

GAF is a feature on the Now Platform that clusters and indexes related records and executes actions on them in agentic AI and Now Assist generative AI. See [Group Action Framework](../concept/group-action-framework.md) for more information about GAF's role in intelligent experiences and how it works.

Now Assist in AI Search is the foundation for GAF's optimized prediction feature. AI Search is the backup search for certain workflows, and if it is not enabled and ready, GAF will not return any results.

You must index every table for each workflow or application you'd like to configure GAF for. For example, if you are configuring GAF for Now Assist for IT Service Management \(ITSM\), you must index the Incident and related tables.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Status**.

    If you see “AI Search is ready,” proceed. If not, request AI Search installation, which can take 2–24 hours.

2.  Install Now Assist for AI Search by installing a Now Assist application.

    For more information, see [Install Now Assist in AI Search](https://www.servicenow.com/docs/access?context=install-now-assist-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Navigate to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table by entering `sn_nowassist_skill_config.list` in the filter navigator.

4.  Search the Now Assist Skill Config table for action strategy skills by searching **Name** is `*action strategy`, and select the action strategy skill for the application you want to configure.

    For example, if you are configuring GAF for Now Assist for ITSM, select the GAF ITSM action strategy record.

    ![Now Assist Skill Config table filtered for skill configs with name contains action strategy](../image/gaf-action-strategy.png)

5.  In the related list, select the Now Assist Skill Config Var Set record.

6.  Set **Semantic Index Name** to the appropriate field for your table.

    To find the field for your table, go to the Semantic Index Configuration \[ais\_semantic\_index\_configuration\] table by entering `ais_semantic_index_configuration.list` in the filter navigator, filter the **Indexed Source** for the table you want to index, and use the value in the **Name** field. For example, the value is **body** for the Incident table.

7.  Navigate to the Semantic Index Configuration \[ais\_semantic\_index\_configuration\] table by entering `ais_semantic_index_configuration.list` in the filter navigator, filter the **Indexed Source** for the table you want to index and the **Semantic Index Name** you configured in the previous step, and set **Active** to `true` to activate the embedding model.

    ![Semantic Index Configuration table filtered for Index Source contains Incident](../image/gaf-sic-is-filtered.png)

8.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Source**, filter the list so that the **Name** is the name of the table you are configuring, and select the record.

9.  Select **Index All Tables**.

    ![Indexed Source record for the Incident table open with a Index All Tables UI action at the top right](../image/gaf-index-tables.png)


## Result

The tables for Now Assist in AI Search for your Now Assist application is indexed based on the appropriate field.

## What to do next

To confirm that indexing has occurred successfully, check the Indexed Source History related list and ensure that both the **Keyword Ingestion State** and **Semantic Ingestion State** are both set to **Indexed**.

Once your tables have been indexed, you can continue to [Configure Group Action Framework](configure-gaf.md) to set up GAF for each application.

