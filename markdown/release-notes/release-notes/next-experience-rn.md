---
title: Next Experience release notes
description: The ServiceNow Next Experience application delivers an intuitive, personalized experience that enables your organization to drive productivity, improve engagement, and inspire learning with the ServiceNow AI Platform. Next Experience was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Next Experience release notes

The ServiceNow® Next Experience application delivers an intuitive, personalized experience that enables your organization to drive productivity, improve engagement, and inspire learning with the ServiceNow AI Platform. Next Experience was enhanced and updated in the Zurich release.

## Next Experience highlights for the Zurich release

-   Customize the visual experience of the Now Assist menu by using the new toggle to switch between standard or wide view.
-   Manage the visibility of page alerts with a new accessibility user preference.
-   Access usage analytic data for applications and web pages directly with the new Usage Analytics utility menu.

See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Lazy loading of Workspace pages user preference available](https://www.servicenow.com/docs/access?context=next-experience-workspace-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Control how your Workspace pages are loaded, either all at once or as needed, by using the new Workspace lazy load user preference. Lazy loading is enabled by default and displays content dynamically, reducing page load times. See the Accessibility information section for additional details.

-   **[Use the menu toggle to view the Now Assist menu in wide mode](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    View the Now Assist menu in wide mode to reduce the need for scrolling and truncating content.

-   **[Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Use a new accessibility preference to keep page alerts visible. See the Accessibility information section for additional details.

-   **[Usage Analytics utility menu available](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Obtain usage analytic data for your applications and web pages with the Usage Analytics utility menu. The Usage Analytics menu appears for those users with the analytics\_viewer role.

-   **[View the number of active calls from the OpenFrame phone icon](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    View the number of active calls from the numbered badge on the OpenFrame phone icon.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

    For existing customers who upgrade to Zurich, use [Theme Builder to publish Coral theme to your instance](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) or [add Coral theme to the Next Experience UX Parent App Theme table](https://www.servicenow.com/docs/access?context=configure-presentation-order-of-themes&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Once enabled by a system administrator, Coral is available for [selection in the user's Theme preference](https://www.servicenow.com/docs/access?context=select-a-theme-in-next-experience&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


## Activation information

Next Experience is a ServiceNow AI Platform feature that is active by default when the user loads or upgrades to the Zurich release. If there are known problems with turning on Next Experience on an instance, an opt-out system property can be created before upgrade.

Theme Builder comes with the Next Experience and is active by default.

## Browser requirements

The Zurich release doesn't support Internet Explorer 11. The iOS version of Firefox is also not supported.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.

-   **[New Accessibility preference added for page alerts](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Turn on the **Do not auto-dismiss page alerts** preference to keep page alerts visible until you manually close them.

-   **[New Workspace preference added to enhance screen reader output for your Workspace pages](https://www.servicenow.com/docs/access?context=next-experience-workspace-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    A new Workspace preference lets you turn off lazy loading for workspace pages. When you turn off lazy loading, the entire page loads at once. This action improves compatibility with screen readers and provides a more consistent and reliable reading experience.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

