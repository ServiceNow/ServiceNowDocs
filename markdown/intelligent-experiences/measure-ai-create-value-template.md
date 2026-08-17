---
title: Create a value template
description: Create a value template to define how AI Control Tower calculates the value delivered by your AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-create-value-template.html
release: australia
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 2
breadcrumb: [Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Create a value template

Create a value template to define how AI Control Tower calculates the value delivered by your AI systems.

## Before you begin

Role required:

-   AI steward \[sn\_ai\_g overnance\_ai\_steward\]
-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

A value template defines the formula which AI Control Tower uses to calculate value: Productivity = Usage × Time × Quality. You create a template in three steps:

1.  **Formula**
2.  **Mapping**
3.  **Test \(optional\)**

The Templates page has three tabs, **All templates**, **Default template rules**, and **AI system mapping**. On the **All templates** tab, each template lists its type \(Custom or OOB\), persona, state \(Draft, Inactive, Published, or Retired\), description, and who last updated it.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and templates** &gt; **Templates**.

2.  On the **All templates** sub-tab, select **Create template**.

    **Note:** The template page opens the **All templates** tab by default.

3.  For each of the three steps, fill in the fields on the forms.

    For descriptions of the field values, see [Value template form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-ai-reference-value-template-form.md).

<table id="table_b12_dtb_1kc"><tbody><tr><td>

1: Formula

 To build calculation.

</td><td>

Add the template details.

 Select **Add metrics** to use a custom metric for calculations. See [Create an automated indicator with a wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/t_CrtIndctrIndctrWzrd.md) for more information.

 \[Omitted image "measure-ai-create-value-template-formula.png"\] Alt text: Formula section in the Create value template form in AI Control Tower

 Select **Next**.

</td></tr><tr><td>

2: Map

 To select assets.

</td><td>

Select the type of AI asset and AI assets that you want to map to the value template.

 \[Omitted image "measure-ai-create-value-template-map.png"\] Alt text: Map section in the Create value template form in AI Control Tower

 Select **Next**.

**Note:** You can select **back** and change the selected AI assets.

</td></tr><tr><td>

3: Test

 To preview value estimate.

 **Note:** Step 3 to test is optional. Users can choose to skip this step and publish the template after mapping with assets.

</td><td>

Select the instance and AI assets for which you want to estimate the real-time value in productivity and select **Validate and calculate**.

 \[Omitted image "measure-ai-create-value-template-test.png"\] Alt text: Test section in the Add value template form in AI Control Tower

</td></tr></tbody>
</table>4.  Select **Publish template**.

    The Publish template dialogue box appears if any of the selected AI assets already have a mapping with an existing value template and a confirmation message is displayed whether to publish the template.

    **Note:**

    No AI system can have two templates for its value calculation.

    When a value template is published, it’s modified across all instances and subsequent calculations are based on the new template.


## Result

A new value template has been created and is available in the **Templates** list.

