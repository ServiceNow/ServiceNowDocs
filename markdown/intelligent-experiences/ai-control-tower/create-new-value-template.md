---
title: Create a new value template
description: Add a value template to define, calculate, and track the value delivered by an AI asset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-new-value-template.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 1
breadcrumb: [Using value templates, Use, AI Control Tower, Enable AI experiences]
---

# Create a new value template

Add a value template to define, calculate, and track the value delivered by an AI asset.

## Before you begin

Role required: AI steward \[sn\_ai\_g overnance\_ai\_steward\] and AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to **Productivity** &gt; **Value templates**.

4.  Select **New template**.

5.  On the Add value template form, fill in the fields.

    For a description of the field values, see [Add value template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/add-value-template-form.md).

<table id="table_lzy_xkt_jhc"><tbody><tr><td>

1. Formula

 To build calculation.

</td><td>

Select **Add metrics** to use a custom metric for calculations. See  for more information.

 \[Omitted image "aict-create-new-value-template-formula.png"\] Alt text: Formula section in the Add value template form in AI Control Tower.

 Select **Next**.

</td></tr><tr><td>

2. Map

 To select assets.

</td><td>

Select the type of AI asset and AI assets that you want to map to the value template.

 \[Omitted image "aict-create-new-value-template-map.png"\] Alt text: Map section in the Add value template form in AI Control Tower.

 Select **Next**.

**Note:** You can select **back** and change the selected AI assets.

</td></tr><tr><td>

3. Test

 To preview value estimate.

**Note:** Step 3 to test is optional. Users can choose to skip this step and publish the template after mapping with assets.

</td><td>

Select the instance and AI assets for which you want to estimate the real-time value in productivity and click **Validate and calculate**.

 \[Omitted image "aict-create-new-value-template-test.png"\] Alt text: Test section in the Add value template form in AI Control Tower.

</td></tr></tbody>
</table>6.  Select **Publish template**.

    The Publish template dialogue box appears if any of the selected AI assets already have a mapping with an existing value template and a confirmation message is displayed whether to publish the template.

    **Note:**

    No AI system can have two templates for its value calculation.

    When a value template is published, it’s modified across all instances and subsequent calculations are based on the new template.

    A new value template has been created and is available in the **Value templates** list.


**Parent Topic:**[Using value templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/using-value-templates.md)

