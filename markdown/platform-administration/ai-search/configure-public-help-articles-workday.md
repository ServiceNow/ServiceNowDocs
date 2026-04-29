---
title: Configure access to help articles in Workday
description: Create an article audience rule in Workday and specify it for your help articles to make them accessible by all your employees. The Workday external content connector uses the audience rule and article settings to make content and metadata from your help articles searchable.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure access to help articles in Workday

Create an article audience rule in Workday and specify it for your help articles to make them accessible by all your employees. The Workday external content connector uses the audience rule and article settings to make content and metadata from your help articles searchable.

## Before you begin

You need administrator privileges in your organization's Workday tenant.

Role required: none

## About this task

This task is optional. By default, the Workday external content connector retrieves searchable content and metadata from help articles that are accessible by all your organization's employees in Workday. To facilitate this retrieval, you need to create an article audience rule and then apply that rule to each article that you want to make searchable.

If you don't want the connector to retrieve searchable content and metadata from help articles in Workday, you can skip this task.

## Procedure

1.  Create a new article audience rule in Workday.

    1.  Log in to your Workday tenant with your administrator credentials.

    2.  In the Workday search bar, search for the **Create Article Audience Rule** task and select it.

    3.  On the Create Article Audience Rule page, in the Description field, enter `Public` as the description for your new article audience rule.

    4.  In the Rule Conditions table, select **+** to add a new rule condition row, then enter the following field values.

        |Field|Value|
        |-----|-----|
        |And/Or|And|
        |Source External Field or Condition Rule|Worker is Employee|
        |Relational Operator|equal to|
        |Comparison Type|Value specified in this filter|
        |Comparison Value|Yes|

    5.  In the Rule Conditions table, select **+** to add a second new rule condition row, then enter the following field values.

        |Field|Value|
        |-----|-----|
        |And/Or|Or|
        |Source External Field or Condition Rule|Worker is Contingent Employee|
        |Relational Operator|equal to|
        |Comparison Type|Value specified in this filter|
        |Comparison Value|Yes|

    6.  Select **OK**.

        Workday creates your new article audience rule.

2.  Create an audience record for your new article audience rule.

    1.  In the Workday search bar, search for the **Maintain Article Audiences** task and select it.

    2.  On the Maintain Article Audiences page, in the Audiences table, select **+** to add a new audience row.

    3.  In the Name field, enter `Public` as the name for your new audience row.

    4.  In the Who Can View field, select your **Public** article audience rule.

    5.  Select **OK**.

    Workday creates your new audience record.

3.  Perform these steps for each article that you want to make searchable through the Workday external content connector.

    1.  In the Workday search bar, search for the **Edit Article** task and select it.

    2.  On the Edit Article page, in the Article field, search for and then select the article that you want to make accessible by all your organization's employees.

    3.  On the article page, select **Edit**.

    4.  In the Settings pane, in the Who Can View field, select **Public**.

    5.  Select **Publish**.

    Workday republishes the article, making it accessible by all your organization's employees.


**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

