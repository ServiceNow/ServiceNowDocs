---
title: Configure the Registration and Login Pages for GOV.UK Design System Service Portal
description: The GOV.UK Developer Toolkit provides default GDS Service Portal registration and login pages that are complaint with GOV.UK design standards. You can use these pages as-is, or you can configure the default widgets to meet your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gds-registlogin.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure pages, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Registration and Login Pages for GOV.UK Design System Service Portal

The GOV.UK Developer Toolkit provides default GDS Service Portal registration and login pages that are complaint with GOV.UK design standards. You can use these pages as-is, or you can configure the default widgets to meet your needs.

## Branded Landing page

Upon accessing the portal homepage as a non-authenticated user, a user is shown a branded landing page, where they have the option to log in or register for the GDS Service Portal. This pre-login page contains a login button in the header, and a link to the registration page for users that don't have a record in the system..

\[Omitted image "psds\_uk\_gds\_landing.png"\] Alt text: GDS Portal Branded Landing page.

## Login Page

When a user selects Log-in on this landing page, they are directed to the default GDS Service Portal login page. The default login page \(uk\_gds\_login\) contains the UK GDS Login widget, which provides a field for users to enter their credentials for log-in to the GDS Service Portal. This widget uses credentials from the User \[sys\_user\] record.

\[Omitted image "psds\_uk\_gds\_login.png"\] Alt text: GDS Portal login page.

This login page can be customized using widgets, and you can define different login scenarios that will redirect user to certain pages on authentication. For more information on customizing login scenarios in a portal, see .

## Registration Pages

When a user selects Register on this page, the default GDS Service Portal registration page \(uk\_gds\_register\) displays. The default registration page contains the following widgets:

-   UK GDS Registration Content widget, which displays "value proposition" card showing a heading, subtitle, and a list of benefits to encourage users to register
-   UK GDS Registration Info widget, which renders a "Create an account" card with registration type options \( constituent, business contact, new business\). Selecting a type within this widget will navigate to the registration page for that type, each with distinct widgets or forms that can be customized or replaced.

Authenticated users are redirected to the portal homepage.

\[Omitted image "psds\_uk\_gds\_register.png"\] Alt text: GDS Portal register page.

The default Constituent registration page \(uk\_gds\_constituent\_register\) contains the UK GDS Registration Request widget, which displays a field that captures email, first name, last name, phone \(optional\), password, and acceptance of the terms and conditions. The default business registration page \(uk\_gds\_business\_register\) contains the UK GDS Business Registration widget, which displays a multi-section registration form allowing users to register a new business, and creates a `sn_gsm_business_registration` record. The business contact registration page \(uk\_gds\_business\_contact\_register\) contains the UK GDS Business Contact Registration widget, which displays a "Create an account" form allowing users to register as a business contact, creating a `sn_customerservice_registration`record.

These pages and forms adhere to GOV.UK form patterns using single-column layout, inline validation via `ukgds-error-message`, error summary via `ukgds-error-summary`, reCAPTCHA, and a terms &amp; conditions checkbox.

For more information on how to edit widgets that appear on a page in the Service Portal Designer, see [Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md). For more information on portal pages, see .

**Parent Topic:**[Configure the GOV.UK Design System Service Portal Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.md)

