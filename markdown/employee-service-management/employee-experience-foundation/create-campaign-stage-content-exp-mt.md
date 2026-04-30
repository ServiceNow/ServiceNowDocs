---
title: Create Microsoft Teams campaign stages using the Campaign Builder Experience
description: Use the Campaign Experience Builder to create stages for your campaign. Campaign builder provides a simple, single-page view for managing content and assembling your campaign.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create Microsoft Teams campaigns with the Content Experience Builder, Sending notifications to employees using Microsoft Teams, Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create Microsoft Teams campaign stages using the Campaign Builder Experience

Use the Campaign Experience Builder to create stages for your campaign. Campaign builder provides a simple, single-page view for managing content and assembling your campaign.

## Before you begin

Role required: sn\_ca.campaign\_manager or sn\_cd.content\_admin

## About this task

For information about campaigns and campaign bundles and stages, see [Creating campaigns](../../employee-center/concept/ecpro-campaigns.md).

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select the campaign.

3.  From the Campaign Bundles related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Title|Name of the campaign bundle.|
    |Campaign|Option to choose a campaign that is associated with the campaign bundle.|
    |Trigger type|Option to choose a trigger type that determines how the campaign bundle starts or ends. To learn more about triggers, see [Campaign bundle triggers](../../employee-center/reference/ecpro-triggers.md)|
    |Offset trigger start|Enables you to move the end date forward or backward from the value in the **Trigger type** field.|
    |Specify end|Indicates whether you want the campaign bundle to have a specific end.|
    |Description|Brief description for the campaign bundle.|

5.  Select **Submit**.

6.  From the Campaign Content related list, select **New**.

7.  On the form, fill in the fields.

<table id="table_r4b_jpp_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content

</td><td>

Description of the content record.

</td></tr><tr><td>

Campaign Bundle

</td><td>

The campaign bundle to associate with the content.

</td></tr><tr><td>

Title

</td><td>

Title for the campaign content. This value is automatically updated as per the value in the Content field.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the schedule for content is active and available to employees.

</td></tr><tr><td>

Description

</td><td>

Brief description about the campaign bundle.

</td></tr></tbody>
</table>8.  Select **Submit**.

9.  On the Campaign form, select **Publish**.


## Result

The campaign is delivered to the employees according to the scheduled job timeline.

**Parent Topic:**[Create Microsoft Teams campaigns with the Content Experience Builder](../concept/create-campaign-content-exp-builder-mt.md)

