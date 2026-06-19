---
title: Configure the GOV.UK Design System Service Portal Pages
description: By default, the GOV.UK Developer Toolkit supplies you with pages that can be used as-is, or customized by adding and removing widgets in Service Portal Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 8
breadcrumb: [Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Pages

By default, the GOV.UK Developer Toolkit supplies you with pages that can be used as-is, or customized by adding and removing widgets in Service Portal Designer.

## Portal pages

Use portal pages to organize content and design portal user experiences for your constituents. A page provides the base structure for how a collection of information is displayed in the constituent-facing GOV.UK Design System Service Portal. Pages house elements such as layouts, patterns, containers and rows \(which, in turn, house widgets\), and other components to display information. By manipulating the layout of the page and the widgets within it, you can construct the desired user experience and display the information your user needs to access.

-   Pages are referenced using the page ID.
-   Pages and its widgets can be referenced in more than one portal.
-   Use base system pages as templates.

Several pages are included with the GOV.UK Developer Toolkit application for use with the GDS Service Portal. You can use these portal pages as is, or you can customize them to suit your needs. The GDS Service Portal contains the following pages by default:

|Page|Description|
|----|-----------|
|[UK GDS default home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-homepage.md)|This page serves as an entry point to the GDS portal for UK citizens, enabling access to relevant public services, and navigation to high-priority actions, key information, quick links, and case updates.|
|[Registration and Login Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-registlogin.md)|These pages enable a user to register or login to the portal, with different configurable forms and widgets for constituent, business contact, and business, registration.|
|[User Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-profile-page.md)|This page provides the basic structure for UK constituents to view and manage their personal profiles, preferences, and activity history.|
|[Browse Categories Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-browse-cat-page.md)|This page enables UK constituents to view all the public services available to them in the GDS Service Portal.|
|[Case List Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-case-list-page.md)|This page enables UK constituents to view all of their submitted requests for public services.|
|[UK GDS Case Details page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-stdt-page.md)|This page standardizes ticket views across the portal, allows UK constituents to track case status and communications, and staff agents to manage case details and documents.|
|[Configure the GOV.UK Design System Service Portal Knowledge Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-knowl-page-cont.md)|These pages enable UK constituents to browse and search articles and guides, categorized into organized content sections \(Featured, Most Useful, Most Viewed\), without contacting support.|
|[Frequently Asked Questions \(FAQs\) Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-faq-page.md)|This page provides an organized, searchable, and accessible repository of frequently asked questions, enabling users to find answers to common questions about services, submissions, or portal functionality.|
|Record Producer Page|This page enables UK constituents to submit new cases or requests via a GDS-compliant form.|
|[Error pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-error-page.md)|These pages provides the basic structure for GDS-compliant error pages that display error messages with helpful links on a 404, 500, or 503 error.|

Navigate to **All &gt; Service Portal &gt; Pages** to see the Pages \[sp\_page\] table, which displays a list of pages available for use and customization within the portal.

## Create and edit a GDS Service Portal page using Service Portal Designer

By default, the GOV.UK Developer Toolkit supplies you with already-configured pages that contain widgets and other elements that adhere to GDS guidelines, but you can create or edit existing pages to organize the columns that house the widgets and widget instances.

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.
2.  Select **Designer**.
3.  Select UK Government Portal to switch to editing or designing pages for the GDS Service Portal.

    \[Omitted image "psds\_service\_portal\_designer\_select\_portal.png"\] Alt text:

4.  From the Service Portal Designer, select a page to customize, or select **Add a new page**.

    For example, to customize the 503 Service Unavailable error response page for the GDS Service Portal, select **UK GDS 503**.

5.  Edit page properties by selecting **Page** settings in the menu bar.

    Here, you can configure properties such as page title and ID, short description, and add page-specific custom CSS.

6.  **Optional**: Under Layouts, select **Container** and drag it onto the page, then drag one of the other layouts and place it in the container.

    This layout defines the structure of your page and the space available to place widgets. The structure of the layout aligns with the Bootstrap grid template and adds up to 12. If you are editing an existing page and the existing layout of the page meets your needs, you may skip this step.

7.  Edit container properties by selecting the **Container**, then selecting the edit icon \(\[Omitted image "psds\_spd\_pencil\_edit\_icon.png"\] Alt text: edit icon\).

    Here, you can customize properties such as container name, width, CSS class, and the background color or image for that particular container \(and its widgets\).

8.  Use the Widget filter to search for an existing widget, then drag the widget to the container layout to add it to the page.

    Each widget added to a page becomes its own instance. Widget instances get their logic from the base widget template, as well as other set scripts and properties that can be configured specific to that instance. Select the pencil icon \(\[Omitted image "psds\_spd\_pencil\_edit\_icon.png"\]\) to edit an instance of a widget on this page. You may have multiple instances of the same widget on a page, each with different instance options configured. Editing the instance options of a widget does not affect the properties of the base widget template.

    For widgets that do not contain any information by default, you must configure the options for their widget instances before they will appear on a portal page. For more information about configuring widget instance options, see .

    For more information on the library of widgets and other page components that are included with the GOV.UK Developer Toolkit and GDS Service Portal, see [GOV.UK Developer Toolkit GDS Service Portal Widget Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-widget-lib.md).

9.  Select the **Preview** tab to preview your changes to the page, or the \[Omitted image "psds\_spd\_new\_tab\_icon.png"\] Alt text: new tab icon icon to view the edited page in a new tab.

    Your changes save automatically.


**Result**\[Omitted image "psds\_gds\_uk\_503\_page\_layout\_design.png"\] Alt text:

The page is created with, or is edited to include, the desired content and widgets.

-   **[Add a page to the GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-govuk-dev-tk-portal-pages-add.md)**  
Add a page in the GDS Service Portal, to which you can add any combination of GDS-compliant portal widgets from the GOV.UK Developer Toolkit widget library.
-   **[Configure the Registration and Login Pages for GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-registlogin.md)**  
The GOV.UK Developer Toolkit provides default GDS Service Portal registration and login pages that are complaint with GOV.UK design standards. You can use these pages as-is, or you can configure the default widgets to meet your needs.
-   **[Configure the Homepage for GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-homepage.md)**  
By default, the GOV.UK Developer Toolkit provides a homepage that is complaint with GOV.UK design standards. This page contains widgets and other components that enable UK constituents to access cases, announcements, and helpful content, and quick navigation to detailed views and actions. You can use this page as-is, or you can configure the default widgets on the page to meet your needs.
-   **[Configure the GOV.UK Design System Service Portal User Profile page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-profile-page.md)**  
Configure the user profile page using widgets and widget instances, enabling UK citizens to view and manage their personal profiles, preferences, and activity history.
-   **[Configure the GOV.UK Design System Service Portal Services Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-browse-cat-page.md)**  
Configure the Services page, which enables constituents to browse and search catalog items from different service catalogs and categories and see all services available to them.
-   **[Configure the GOV.UK Design System Service Portal Case List page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-case-list-page.md)**  
Configure the case list page.
-   **[Configure the Case Details \(standard ticket\) page for GOV.UK Developer Toolkit GDS Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-stdt-page.md)**  
Configure individual request types to display case Details, the request-specific information shown to constituents when viewing submitted requests. They can view case statuses and request history, and communicate with caseworkers and agents.
-   **[Configure the GOV.UK Design System Service Portal Knowledge Pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-knowl-page-cont.md)**  
The knowledge pages provide the basic, GDS-compliant structure for displaying knowledge base content for constituents using the GDS Service Portal.
-   **[Configure the FAQ page for GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-faq-page.md)**  
Add the Portal FAQ widget to your portal and modify its data, presentation, and behavior. You can use the Portal FAQ widget to display a frequently asked questions list \(FAQ\) from a knowledge table on the portal.
-   **[Configure the Error Pages for GOV.UK Developer Toolkit GDS Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-error-page.md)**  
Use Portal Widgets to configure and customize the error page that is shown when a user encounters errors such as broken links, service issues, or downtime \(404, 500, 503\).

**Parent Topic:**[Configure the GOV.UK Design System \(GDS\) Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gds-content-pack-gsp.md)

