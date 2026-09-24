---
title: Using smart assessment template designer
description: You can create assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart assessments can help you to evaluate various situations, aspects, or records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/using-smart-assessment-template-designer.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Retail questionnaire, Retail store plans, Explore, Retail]
---

# Using smart assessment template designer

You can create assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart assessments can help you to evaluate various situations, aspects, or records.

## Smart assessment template designer

If you have the template manager \[sn\_smart\_asmt.template\_manager\] or assessment admin \[sn\_smart\_asmt.assessment\_admin\] role, you can create and update the assessment templates by navigating to **Workspaces** &gt; **Assessment Workspace** and opening the template designer. Create or update the templates by accessing the Assessment Workspace landing page and selecting the existing unpublished assessment template or selecting **New template**.

The following example shows the assessment workspace landing page where you can view all templates and open the template designer.

\[Omitted image "image.sae-assess-workspace"\] Alt text: Assessment Workspace that lists all published and unpublished assessment templates.

In the template designer, you can view and edit the assessment template details on the **General** tab. From this tab, you can access the Settings page to configure the key settings, like the assessment duration, which sets the time frame for your responders to complete the assessment.

The following example shows the settings page for a draft assessment.

\[Omitted image "image.sae-settings-page"\] Alt text: Configuring the settings for a template.

## Triggering assessments

After you finalize and publish these templates, you can use them to trigger the assessments. For more information on triggering the assessments, see .

**Note:** You can create an assessment only from a published assessment template. If there isn’t an associated active assessment, you can modify and publish these published templates again.

For more information, see  and .

## Adding the instructions and questions to a template

You can add instructions and questions as part of a new assessment template or an existing unpublished assessment template. Add instructions and questions by opening the template designer and navigating to the **Questions** tab. You can input instructions in the instructions text box to help set the clear expectations for your responders. You can also add sections to categorize your questions by different areas. Each section requires a name and specific questions.

The following example shows how to add a section.

\[Omitted image "image.sae-section-form"\] Alt text: Adding a new section.

You can use various types of questions and include a check box, text, date, and more with customizable attributes such as visibility, response, and justification requirements.

The following example shows some question types that you can use.

\[Omitted image "image.sae-question-types"\] Alt text: Question types available for creating an assessment template.

You can use instructions and questions to help gather precise and relevant information from your responders. For more information, see .

## Adding reference information to a template

You can add reference information that assessors can see while they complete the assessment. The reference information can include any live data from the assessment scope. For example, you can include information on any of the associated incidents, work notes, or domain. Adding necessary reference information to assessments can help minimize the need for external references. For more information, see .

## Creating categories for an assessment template

You can add an assessment template category to a new or an existing unpublished assessment template but you must create a template category before it can be used for template data segregation. The template category selected for the assessment template determines who can access the template. You can't complete the creation of template categories within the template designer. To create a template category, navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**. For more information on creating assessment template categories, see .

## Searching in assessment templates

Search for text within the assessment template sections, subsections, or questions. The search results appear in place of the content tree, and the first match is highlighted. If no matches are found, a "No results found" message is displayed. You can select the search icon on the navigation pane to display the search box.

\[Omitted image "image.search-asmnt-ques"\] Alt text: Search icon on assessment navigation pane

**Parent Topic:**[Retail questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-create-a-questionnaire-template.md)

