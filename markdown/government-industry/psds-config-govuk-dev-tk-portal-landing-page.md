---
title: Configure a GOV.UK Design System Service Portal citizen-facing landing page
description: Create a catalog anchor landing page that lets constituents find a question-page journey on the GDS Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-landing-page.html
release: brazil
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure page patterns, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure a GOV.UK Design System Service Portal citizen-facing landing page

Create a catalog anchor landing page that lets constituents find a question-page journey on the GDS Service Portal.

## Before you begin

Role required: admin

## About this task

A question or service request journey lives on its own instance page, and, by default, without an anchor, nothing in the catalog will point at it and render it reachable. Create a catalog anchor item on the services page \(by default, `uk_gds_services`\) to ensure that the question or service request journey appears as a listed catalog item. You can use **Service Portal Designer** to create or copy a page.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Select UK Government Portal to switch to editing or designing pages for the GDS Service Portal.

    \[Omitted image "psds\_service\_portal\_designer\_select\_portal.png"\] Alt text:

4.  From the Service Portal Designer, select an existing GOV.UK journey landing page, and select **Copy**.

5.  Give it a unique page ID, such as `uk_gds_blocked_footpath`.

6.  Update the heading and introductory content.

7.  Configure its Start link to open the dedicated assessment page created for the question journey.

    For more information, see the last step of this procedure: [Configure the GOV.UK Design System Service Portal Question Page Pattern Journey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-govuk-dev-tk-portal-question.md).

8.  Restrict the page to **snc\_external** and/or **snc\_internal**.

    **Note:** Mark the page public **if** anonymous users are allowed to use the service.

9.  To make the journey discoverable from the Services page, create a content item in the Service Catalog by entering the following values:

    |Field|Value|
    |-----|-----|
    |Name|Journey name|
    |Active|true|
    |Content type|External|
    |URL|`?id=<landing_page_id>`|
    |Access type|Restricted|
    |Catalog|UK Government catalog|
    |Category|Appropriate service category|
    |Available on desktop|true|
    |Visible standalone|true|

    Navigate to the **Not Available For** and **Available For** related lists to set the user criteria for the intended audiences. The user criteria can be set to:

    -   users with `SNC External` role to allow both registered and unregistered constituents to access the question or service request journey from the catalog landing page.
    -   users with `snc_internal` role to allow only registered constituents to access the question or service request journey from the catalog landing page.
    **Note:** **Not Available For** overrides **Available For**. Access to the catalog landing page is configured separately.


