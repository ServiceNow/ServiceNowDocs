---
title: Exploring AI Data Kit
description: The AI Data Kit plugin for ServiceNow Otto enables you to add datasets to a data catalog and create collections for use in AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/exploring-now-assist-data-kit.html
release: brazil
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Exploring AI Data Kit

The AI Data Kit plugin for ServiceNow Otto enables you to add datasets to a data catalog and create collections for use in AI Skill Kit.

## AI Data Kit overview

If the base system ServiceNow Otto skills don't fit your needs, use AI Data Kit to create custom datasets and data collections. These can be used in AI Skill Kit for evaluation.

## AI Data Kit users

|User|Description|
|----|-----------|
|AI practitioner|AI practitioners manage data set creation in AI Data Kit. They develop and evaluate skills and other technical solutions for various use cases.|
|Analyst|Analysts confirm data quality for AI development and evaluation. They work with AI practitioners to follow data curation guidelines set for specific AI use cases.|

## AI Data Kit workflow

The following diagram shows the user journey for AI Data Kit.

\[Omitted image "na-data-kit-infographic.png"\] Alt text: ServiceNow Otto AI Data Kit workflow

Two users take part in this workflow. The AI practitioner does most of the work. An analyst can enter and review ground truth values.

1.  [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md) in AI Skill Kit.

2.  [Add records from an instance table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/add-dataset.md) to the data catalog as a dataset. If you don't have suitable records, [generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md) instead.

3.  \(Optional\) [Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md) to work with a smaller set of records.

4.  \(Optional\) Check the dataset before you use it:

    -   [Scan for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/sensitive-data.md) and cleanse what the scan finds.

    -   [View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/view-data-insights.md) to see completeness and distribution.

5.  \(Optional\) [Add a ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/add-ground-truth.md) to each dataset record. The AI practitioner creates the guidelines. An analyst can enter and review the values.

6.  [Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/create-data-collection.md) and add one or more datasets to it.

7.  \(Optional\) Apply a sampling method to choose which records go into the collection.

8.  Publish the data collection.

9.  Return to AI Skill Kit, select the data collection, and run the evaluation.

10. Review the results, iterate on the prompt if needed, and publish the skill.


## AI Data Kit benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Curate records from an instance table into a dataset that you can reuse for AI development and evaluation.|[Add a dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/add-dataset.md)|AI practitioner|
|Create a smaller dataset from an existing one so that you can evaluate a skill without processing every record.|[Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md)|AI practitioner|
|Generate records when you don't have production data, or when using production data raises privacy concerns.|[Generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md)|AI practitioner|
|Scan a dataset for sensitive data, such as names and email addresses, and cleanse what the scan finds.|[Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/sensitive-data.md)|AI practitioner|
|Check the completeness and distribution of a dataset before you use it, so that gaps don't affect your evaluation results.|[View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/view-data-insights.md)|AI practitioner|
|Record the expected output for each record so that an evaluation can compare a skill's response against a known result.|[Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/add-ground-truth.md)|AI practitioner, Analyst|
|Combine one or more datasets into a data collection and publish it for use in AI Skill Kit.|[Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/create-data-collection.md)|AI practitioner|

## What to explore next

To learn more about configuring and using AI Skill Kit, see:

-   [Configuring AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/configuring-now-assist-data-kit.md)
-   [Using AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/using-now-assist-data-kit.md)
-   [AI Data Kit reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/na-data-kit-reference.md)

