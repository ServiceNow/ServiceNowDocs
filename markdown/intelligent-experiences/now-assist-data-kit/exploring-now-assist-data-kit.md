---
title: Exploring AI Data Kit
description: Use AI Data Kit to build, curate, and manage the data that you use to evaluate AI skills and AI agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/exploring-now-assist-data-kit.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 5
breadcrumb: [AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Exploring AI Data Kit

Use AI Data Kit to build, curate, and manage the data that you use to evaluate AI skills and AI agents.

## AI Data Kit overview

Evaluating an AI skill or agent requires data that reflects how it will be used. AI Data Kit gives you one place to build and manage that data. You can add records from instance tables as datasets, or generate synthetic data when you don't have suitable records or can't use them for privacy reasons. AI Data Kit automatically extracts metadata from each dataset, which helps you find and reuse datasets.

Before you use a dataset, you can prepare it for evaluation:

-   Scan for sensitive data, such as names and email addresses, and cleanse what the scan finds.
-   Check the completeness and distribution of the data to find gaps.
-   Filter the dataset to the records that matter for your use case, or create a smaller derived dataset.
-   Add ground truth, which is the expected correct output for each record. In labeling projects, an analyst can enter and review ground truth values.

Datasets and data collections play different roles. A dataset holds records from a single source, such as an instance table or a synthetic data run, and it's where you prepare the data. A data collection packages that data for evaluation. You choose the columns that your skill needs, select or sample the records to include, and can combine records from more than one dataset. When you publish the collection, its contents are frozen, so you can evaluate each revision of a skill against the same data and compare the results.

To evaluate a skill, select the published collection in AI Skill Kit. Ground truth data is also available for agentic evaluation.

## AI Data Kit users

|User|Role|Description|
|----|----|-----------|
|AI practitioner|sn\_data\_kit.admin|AI practitioners create datasets, prepare them for evaluation, and publish data collections. They build and evaluate AI skills and agents.|
|Analyst|sn\_data\_kit.analyst|Analysts enter and review ground truth values and confirm data quality for evaluation. They follow the guidelines that AI practitioners set for each use case.|

## AI Data Kit workflow

The following diagram shows the user journey for AI Data Kit.

\[Omitted image "na-data-kit-infographic.png"\] Alt text: ServiceNow Otto AI Data Kit workflow

Two users take part in this workflow. The AI practitioner does most of the work. An analyst can enter and review ground truth values.

1.  [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-new-skill.md) in AI Skill Kit.

2.  Add records from an instance table as a dataset. If you don't have suitable records, [generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md) instead.

3.  \(Optional\) [Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md) to work with a smaller set of records.

4.  \(Optional\) Check the dataset before you use it:

    -   [Scan for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md) and cleanse what the scan finds.

    -   [View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/view-data-insights.md) to see completeness and distribution.

5.  \(Optional\) [Add a ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md) to each dataset record. The AI practitioner creates the guidelines. An analyst can enter and review the values.

6.  [Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md) and add one or more datasets to it.

7.  \(Optional\) Apply a sampling method to choose which records go into the collection.

8.  Publish the data collection.

9.  Return to AI Skill Kit, select the data collection, and run the evaluation.

10. Review the results, iterate on the prompt if needed, and publish the skill.


## AI Data Kit benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Curate records from an instance table into a dataset that you can reuse for AI development and evaluation.||AI practitioner|
|Create a smaller dataset from an existing one so that you can evaluate a skill without processing every record.|[Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md)|AI practitioner|
|Generate records when you don't have production data, or when using production data raises privacy concerns.|[Generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md)|AI practitioner|
|Scan a dataset for sensitive data, such as names and email addresses, and cleanse what the scan finds.|[Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md)|AI practitioner|
|Check the completeness and distribution of a dataset before you use it, so that gaps don't affect your evaluation results.|[View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/view-data-insights.md)|AI practitioner|
|Record the expected output for each record so that an evaluation can compare a skill's response against a known result.|[Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md)|AI practitioner, Analyst|
|Combine one or more datasets into a data collection and publish it for use in AI Skill Kit.|[Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md)|AI practitioner|

## What to explore next

To learn more about configuring and using AI Skill Kit, see:

-   [Configuring AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/configuring-now-assist-data-kit.md)
-   [Using AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/using-now-assist-data-kit.md)
-   [AI Data Kit reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-reference.md)

