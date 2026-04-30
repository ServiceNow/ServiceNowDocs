---
title: Add or update a tag value for an AI Service tag category
description: Associate a tag name with its corresponding tag value whenever a new AI service or a category within an existing AI service is introduced for Amazon Web Services \(AWS\), Microsoft Azure, or Google Cloud Platform \(GCP\).
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add or update a tag value for an AI Service tag category

Associate a tag name with its corresponding tag value whenever a new AI service or a category within an existing AI service is introduced for Amazon Web Services \(AWS\), Microsoft Azure, or Google Cloud Platform \(GCP\).

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## About this task

**Important:** This feature is available with the Cloud Cost Management 8.0.0 version or later.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags**.

2.  Select **Tag categories**.

3.  On the Tag categories page, select the **AI Service** tag category.

4.  On the AI Service page, select the **Tag name value** tab.

5.  Select **Add/Update tag values**.

6.  In the **Add/Update AI Service tag values** dialog box, select the **Create** tab.

7.  Select the service provider tag name and provide a tag value.

    -   For AWS, add the lineItem/ProductCode as the tag value against the AWS AI service tag name **sn\_ccm\_aws\_ai\_service**.
    -   For Azure, add the Meter Category name as the tag value against the Azure AI service tag name **sn\_ccm\_azure\_ai\_service**.
    -   For GCP, add the Service description name as the tag value against the GCP AI service tag name **sn\_ccm\_gcp\_ai\_service**.
8.  Select **Submit**.

9.  If you want to update the tag value of an AI service that you have created, select **Add/update tag values**.

    **Note:** You can't update the tag values for the default cloud categories for managing AI services. To view the default cloud categories for managing AI services within the Machine Learning service category, see [List of default Cloud categories for AI services](../reference/ai-service-provider-list.md).

    1.  Select the **Update** tab.

    2.  Select the provider tag name.

        For example, select **sn\_ccm\_aws\_ai\_service**.

    3.  Select the tag value that you want to update.

        For example, select **Amazon Test**.

    4.  Provide a new tag value for it.

        For example, change the existing tag value to **Amazon Test 2**.

    5.  Select **Submit**.


## Result

After a tag name is associated with its corresponding tag value, you can view the spend data of the AI service you added on the Spend analytics page. For more information, see [Spend analytics](../concept/spend-anaytics.md).

## What to do next

After you add a tag value for an AI Service tag category, you must reimport the billing data to generate the spend for the added tag.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

**Related topics**  


[Tags and tag categories](../reference/tags-overview.md)

[Create and update a tag category](tag-category-crud-cloudin.md)

[Schedule and manage the jobs that download AWS billing data](aws-bill-dwnld-job-cloudin.md)

[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

[Schedule and manage the jobs that download Google Cloud billing data](gcp-bill-dwnld-job-cloudin.md)

