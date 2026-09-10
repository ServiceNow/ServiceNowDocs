---
title: Service Portal release notes
description: The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Service Portal release notes

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.

## About Service Portal

-   Analyze the performance of portal pages and their widgets.
-   Compare cloned widgets with the base widget from which they were cloned.
-   Use ECMAScript 2021 \(ES12\) JavaScript mode in widget server scripts.
-   Enable early single sign-on \(SSO\) redirection.
-   Specify the user roles that apply to a page route map.

See [Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/c_ServicePortal.md) for more information.

## Activation and other requirements

-   **Activation information**

    Service Portal is a ServiceNow AI Platform feature that is active by default.

-   **Browser requirements**

    The Yokohama release doesn't support Internet Explorer 11.

    The iOS version of Firefox doesn’t support Service Portal pages.

    For more information about Service Portal browser support, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/browser-support.md).


**Parent Topic:**[ServiceNow AI Platform user interface release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-ui-rn-landing.md)

## Yokohama

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with an easy-to-use, modular portal framework. Service Portal was enhanced and updated in the Yokohama release.

### What's new

-   **[Analyze the performance of portal pages and their widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/analyze-page-performance.md)**

    Set benchmarks against which to analyze the performance of a portal page. Identify widgets on the page that don't meet the performance benchmarks and view details about their performance.

-   **[Compare a cloned widget with its base widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/compare-with-base-system.md)**

    Compare cloned widgets with the base widget from which they were cloned. View differences between the code of the cloned widget and the base widget highlighted in the code comparator.


### What's changed

-   **[Use ECMAScript 2021 \(ES12\) JavaScript mode in server scripts for widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/widget-dev-guide.md)**

    Use features supported in the ECMAScript 2021 \(ES12\) JavaScript mode in server-side scripts for widgets by selecting **Turn on ECMAScript 2021 \(ES12\) mode** from the widget record or Widget Editor. For information about features supported in the ECMAScript 2021 \(ES12\) JavaScript mode, see .

-   **[Define roles for page route maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/reroute-page.md)**

    Control which users are redirected to a new page based on a page route map. Specify the user roles to apply in the Page Route Map form.

-   **[Improved redirection for single sign-on \(SSO\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/c_SPSSOLoginAndRedirects.md)**

    Improved the experience of logging in to portals that use single sign-on \(SSO\) authentication by redirecting to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

-   **[Enforce providing comments when rejecting requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/approvals-widget.md)**

    Require approvers to provide comments when rejecting a request from the Approvals widget. Administrators can enable requiring comments from the widget instance options.

-   **[Check cross-scope privileges to a table with the Form widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/form-widget.md)**

    Validate access to tables from which the Form widget fetches data. The Form widget checks for the necessary cross-scope privileges to a table by default.


