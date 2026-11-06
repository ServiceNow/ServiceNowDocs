---
title: Using AI Data Kit
description: Use AI Data Kit to add or generate datasets, prepare them for evaluation, and publish them in data collections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/using-now-assist-data-kit.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: concept
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Using AI Data Kit

Use AI Data Kit to add or generate datasets, prepare them for evaluation, and publish them in data collections.

## Overview of AI Data Kit

Start by adding a dataset or generating synthetic data. The other tasks work on an existing dataset, and you can do them in whatever order suits your evaluation. When the data is ready, package it in a data collection for evaluation.

-   ****

    Add records from an instance table, or import a file from your computer. When you add a dataset, you can also choose to scan it for sensitive data.

-   **[Generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md)**

    Generate synthetic records when you don't have suitable data or can't use it for privacy reasons. If you have records to use as examples, see . Otherwise, see .

-   **[Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md)**

    Create a smaller dataset from an existing one by selecting records manually or by sampling. A smaller dataset lets you evaluate a skill without processing every record.

-   **[Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md)**

    Scan a dataset for sensitive data, such as names and email addresses, and cleanse what the scan finds. Scanning requires the Data Privacy plugins.

-   **[View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/view-data-insights.md)**

    Check the completeness and distribution of the values in a dataset.

-   **[Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md)**

    Add the expected correct output for dataset records, so that an evaluation can compare responses against a known result. You set the guidelines, and an analyst can enter and review the values.

-   **[Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md)**

    Package one or more datasets for evaluation by choosing the columns and records to include. After you publish the collection, you can select it in AI Skill Kit to evaluate a skill.


