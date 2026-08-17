---
title: Service Portal release notes
description: The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Service Portal release notes

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.

## Service Portal highlights for the Yokohama release

-   Analyze the performance of portal pages and their widgets.
-   Compare cloned widgets with the base widget from which they were cloned.
-   Use ECMAScript 2021 \(ES12\) JavaScript mode in widget server scripts.
-   Enable early single sign-on \(SSO\) redirection.
-   Specify the user roles that apply to a page route map.

See  for more information.

## New in the Yokohama release

-   **Analyze the performance of portal pages and their widgets**

    Set benchmarks against which to analyze the performance of a portal page. Identify widgets on the page that don't meet the performance benchmarks and view details about their performance.

-   **Compare a cloned widget with its base widget**

    Compare cloned widgets with the base widget from which they were cloned. View differences between the code of the cloned widget and the base widget highlighted in the code comparator.


## Changed in this release

-   **Use ECMAScript 2021 \(ES12\) JavaScript mode in server scripts for widgets**

    Use features supported in the ECMAScript 2021 \(ES12\) JavaScript mode in server-side scripts for widgets by selecting **Turn on ECMAScript 2021 \(ES12\) mode** from the widget record or Widget Editor. For information about features supported in the ECMAScript 2021 \(ES12\) JavaScript mode, see .

-   **Define roles for page route maps**

    Control which users are redirected to a new page based on a page route map. Specify the user roles to apply in the Page Route Map form.

-   **Improved redirection for single sign-on \(SSO\) authentication**

    Improved the experience of logging in to portals that use single sign-on \(SSO\) authentication by redirecting to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

-   **Enforce providing comments when rejecting requests**

    Require approvers to provide comments when rejecting a request from the Approvals widget. Administrators can enable requiring comments from the widget instance options.

-   **Check cross-scope privileges to a table with the Form widget**

    Validate access to tables from which the Form widget fetches data. The Form widget checks for the necessary cross-scope privileges to a table by default.


## Activation information

Service Portal is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

The Yokohama release doesn't support Internet Explorer 11.

The iOS version of Firefox doesn’t support Service Portal pages.

For more information about Service Portal browser support, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/browser-support.md).

## Related ServiceNow applications and features

-   **Sitemap Generator**

    Define and automatically generate XML sitemaps to improve the search engine optimization \(SEO\) of your public portal pages.

-   **AI Search**

    The ServiceNow AI Search application provides search capabilities for Service Portal, Now Mobile, and Virtual Agent.

-   **User Experience Analytics**

    After you enable User Experience Analytics for Service Portal, you can view detailed key performance indicator \(KPI\) data on a dashboard and on list views.

-   **Authentication**

    Validate the identity of users who access an instance and allow them to use features that match their role or job function. You can allow portal users to log in without a password by enabling PIV/CAC card authentication.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-ui-rn-landing.md)

