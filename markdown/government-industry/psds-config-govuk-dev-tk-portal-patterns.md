---
title: Configure the GOV.UK Design System Service Portal Page Patterns
description: Configurable page patterns are best-practice design solutions that combine reusable components to help users complete specific, goal-oriented actions through government services. By default, the GOV.UK Developer Toolkit comes with a pattern library that conforms to the Gov.UK Design System guidelines, and can be copied and used for specific user tasks. Use the base system example page included with the GDS Service Portal to get started configuring with patterns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-patterns.html
release: brazil
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Page Patterns

Configurable page patterns are best-practice design solutions that combine reusable components to help users complete specific, goal-oriented actions through government services. By default, the GOV.UK Developer Toolkit comes with a pattern library that conforms to the Gov.UK Design System guidelines, and can be copied and used for specific user tasks. Use the base system example page included with the GDS Service Portal to get started configuring with patterns.

Page patterns let you combine different configurable components to help a constituent using your services to complete a task. That task might involve entering information, like an address, household information, or ID number, or it might involve helping users upload a file or submit a request. Patterns can be used to request specific information or actions from constituents, to guide them in completing tasks or confirming details, or simply to relay a message or provide information.

Patterns often use one or more reusable components, such as widgets or catalog items, and explain how they are adapted to the context. You can use the base system patterns provided with the GOV.UK Developer Toolkit in their default state, or you can clone, modify, or develop custom page pattern journeys to better fit your needs.

There are two pages available for use with the GDS Service Portal that conform to the Gov.UK page pattern guidelines:

-   Report an abandoned vehicle
-   Report a missed waste collection

Both sample tiles should appear on the catalog page by default, alongside the two record producers they sit next to.

## Step-by-Step navigation journey pattern \(widget\)

The step-by-step navigation page pattern guides users through an end-to-end user flow in sequential stages, with each step providing links to the content needed to complete that step. Step-by-step navigation is useful when:

-   A user is completing a journey that has a specific start and end point
-   There are steps that require the user to engage with multiple guidance elements or complete multiple transactions
-   The steps or tasks need to be completed in a specific order

A step-by-step navigation journey can link guidance and information from different sources, agencies, and services, and can be completed in either a single session, or allow a user to return to the navigation at multiple points in time. In the GOV.UK Developer Toolkit, it is presented as a GDS Service Portal reusable widget that conforms to the Gov.UK Design System page pattern, containing numbered, collapsible steps, each with one or more task links out to a question-page journey, record producer, portal page, KB article, external service, or offline action. This widget can be enabled and customized, and can either be rendered in the right-hand sidebar of pages that are part of the step-by-step navigation, or displayed on a page as a standalone.

For more information on how to configure and customize the step-by-step navigation pattern widgets, see [Add a step-by-step navigation widget to a GOV.UK Design System Service Portal page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-govuk-dev-tk-step-by-step-nav-edit.md)

## Question journey pattern

The question journey page pattern is a forms experience where the questions are surfaces one by one on the UI, and the user can see their responses at the bottom and make changes to them. In the GDS Service Portal, this pattern is followed whenever you need to ask users questions within the service, and must include a back link, page heading, and continue button. It asks one question per page, ensuring that users are presented with a clear goal for each interaction.

For more information on configuring question journeys and page patterns, see [Configure the GOV.UK Design System Service Portal Page Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-govuk-dev-tk-portal-patterns.md).

## Confirmation pattern

Confirmation pattern pages are ones where a user sees the confirmation page after submitting their answer to the last question.

