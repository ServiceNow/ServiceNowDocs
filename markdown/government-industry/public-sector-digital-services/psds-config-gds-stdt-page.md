---
title: Configure the Case Details \(standard ticket\) page for GOV.UK Developer Toolkit GDS Service Portal
description: Configure individual request types to display case Details, the request-specific information shown to constituents when viewing submitted requests. They can view case statuses and request history, and communicate with caseworkers and agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-stdt-page.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Case Details \(standard ticket\) page for GOV.UK Developer Toolkit GDS Service Portal

Configure individual request types to display case Details, the request-specific information shown to constituents when viewing submitted requests. They can view case statuses and request history, and communicate with caseworkers and agents.

The standard ticket case details page provides UK citizens with updates on their submitted cases. Citizen users can view case status, last updated timestamp, and communication history on the Case Detail Page.

To display the related information, you can configure the standard ticket page for requested services on the GDS Service Portal. This configuration verifies a consistent experience when viewing submitted requests in the portal. For example, in the GDS Service Portal, you can access the ticket page for a requested service using the **Your Cases** option from the main menu header.

The information displayed in each section of a standard ticket page depends on the individual request type. If a configurable section has no specified values or if a user doesn’t have access to the information, it isn’t visible. For new GDS Service Portal instances, the standard ticket page is available by default.

\[Omitted image "psds\_uk\_gds\_case\_details\_stdt.png"\] Alt text: Standard ticket page for a GDS Service Portal record producer

## Header Widget

By default, this header widget instance displays the following information on the standard ticket page for a submitted service request:

-   Identification number
-   Created and updated dates
-   State.

    **Note:** Instead of the State field, you can also configure any other field that represents the state of the ticket.


To customize the content of this header widget instance, navigate to **All****Service Portals****Service Portal Configuration****Designers**. Confirm that **UK Government Portal** is the portal selected.

## Info Widget

If configured, this section displays the following regions for a submitted request:

-   Case description with the short description, and optionally the description.

    **Note:** You can map the Description field to any other field on the record.

-   Actions region
-   Case details

## Tab Widget

This widget displays the following tabs for a submitted request, allowing constituents to switch between views and navigate case sections. Each tab is a widget instance.

-   Activity
-   Attachments

You can configure the tabs for standard ticket page. For more information, see .

## Customization

You can configure the case details page components, including toggling widgets, customizing header and footer content, and managing breadcrumb navigation to reflect case hierarchy. For more information on how to edit widgets that appear on a page in the Service Portal Designer, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). For more information on portal pages, see .

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

