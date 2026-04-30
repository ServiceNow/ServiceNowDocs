---
title: Using the template designer
description: You can create assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart assessments can help you to evaluate various situations, aspects, or records.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Using the template designer

You can create assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart assessments can help you to evaluate various situations, aspects, or records.

## Overview of using the template designer

If you have the template manager \[sn\_smart\_asmt.template\_manager\] or assessment admin \[sn\_smart\_asmt.assessment\_admin\] role, you can create and update assessment templates by navigating to the Assessment Workspace landing page. You can create a template by selecting the **New template** button and update an assessment template by selecting an existing unpublished assessment template from the Assessment templates list.

The following example shows the Assessment Workspace landing page, where you can view all templates and open the template designer.

![Assessment Workspace landing page that lists all published and unpublished assessment templates. There's a callout for the New template button.](../image/sae-assess-workspace.png "Assessment Workspace landing page")

In the template designer, you can view and edit the assessment template details on the **General** tab. From this tab, you can access the Settings page to configure the key settings. For example, configuring the assessment duration sets the time frame for your responders to complete the assessment.

## Adding instructions and questions to a template

Instructions help you set clear expectations for your responders, and questions help you gather precise and relevant information from your responders. You can add instructions and questions to a new assessment template or an existing assessment template. You can add sections to categorize your questions by different areas. Each section requires a name and specific questions.

You can choose from the following question types:

-   Text question
-   Drop-down list question
-   Radio button question
-   Check box question
-   Number question
-   Reference question
-   Attachment question
-   Date question

You can also customize the attributes of the question, such as its visibility conditions, setting up default automated response, and justification requirements to ensure well-supported answers.

![Question types available for creating an assessment template.](../image/sae-question-types.png "Question types")

You can use instructions and questions to help gather precise and relevant information from your responders. For more information, see [Add instructions and questions to an assessment template](../task/sae-asmnt-template-populate.md).

## Adding reference information to a template

You can add reference information that assessors can see while they complete the assessment. The reference information can include any live data from the assessment scope. For example, you can include information on any of the associated incidents, work notes, or domain. Adding necessary reference information to assessments can help minimize the need for external references. For information on how to add reference information, see [Add reference information to an assessment template](../task/sae-asmnt-add-reference.md).

## Creating categories for an assessment template

Template categories determine who can access the template. Before you can add an assessment template category to a new or existing unpublished assessment template, you must make a template category. You can't create a template category within the template designer, and after a template is associated with a template category, you can't update it. For information on how to create assessment template categories, see [Create an assessment template category](../task/sae-asmnt-template-category-create.md).

## Searching within assessment templates

Search for text within the assessment template sections, subsections, or questions. The search results appear in place of the content tree, and the first match is highlighted. If no matches are found, a `No results found` message is displayed. You can select the search icon ![](../../../common/image/List_SearchIcon.png) in the navigation pane to display the search box.

## Triggering assessments

After you finalize and publish these templates, you can use them to trigger the assessments. For more information on triggering the assessments, see [Triggering assessments](sae-asmnt-triggering.md).

**Note:** You can create an assessment template only from a published assessment. If there isn’t an associated active assessment, you can modify and publish these published templates again.For more information, see [Accessing templates in the Assessment Workspace](sae-asmnt-workspace.md) and [Create an assessment template](../task/sae-asmnt-template-create.md).

