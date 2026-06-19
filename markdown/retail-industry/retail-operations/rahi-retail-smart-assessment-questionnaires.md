---
title: Smart Assessment questionnaires for Retail
description: Smart Assessment enables users with the sn\_rtl\_hq\_ops.plan\_author role to create smart assessment templates and associate them with store tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/retail-operations/rahi-retail-smart-assessment-questionnaires.html
release: australia
product: Retail Operations
classification: retail-operations
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Retail questionnaire, Retail store plans, Explore, Retail]
---

# Smart Assessment questionnaires for Retail

Smart Assessment enables users with the sn\_rtl\_hq\_ops.plan\_author role to create smart assessment templates and associate them with store tasks.

Use Smart Assessment templates to enhance questionnaires for a Now Mobile Agent application.

Use the Smart Assessment Engine template designer to do the following:

-   Create and customize the assessment templates for questionnaires.
-   Set the assessment parameters such as the question types, justifications, and conditional visibility.
-   Configure conditional questions based on responses of all other types of questions and across sections.

For more information, see [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

## Configuration overview

For information on setting up Smart Assessment, see [Activate and enable Smart Assessment for Field Service questionnaire](https://www.servicenow.com/docs/r/DBkKvgbNn2vmEpXdLk9O2w/_kCg_lZ8PDwWQQ_OHiJOAw).

## Assessment Reader Role Field in Smart Assessment Templates

The **Assessment Reader Role** field determines which users can view questionnaire responses submitted by store associates. When responses must be accessible to other users, this field is configured in **Settings** &gt; **General** on the Questionnaire Authoring page. Users assigned to the specified role can access the submitted responses.

HQ Communication Use Case: For scenarios where plan authors need visibility into submitted Smart Assessment responses, the sn\_rtl\_hq\_ops.plan\_author role can be leveraged, as the required persona already contains this role.

The  **Assessment Reader Role ** field determines which users can view questionnaire responses submitted by fulfillers.

## Category-based access to templates

Control access to templates using roles defined on the Category record.

The HQ Communication category is a predefined category configured with the role sn\_rtl\_hq\_ops.plan\_author.

Users with this role can:

-   Access the HQ Communication category
-   View and use templates associated with the category
-   Create and manage templates within the category, based on additional permissions

**Parent Topic:**[Retail questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/retail-operations/rahi-retail-create-a-questionnaire-template.md)

