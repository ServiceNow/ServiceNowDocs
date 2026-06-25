---
title: Builders' accessibility features and updates
description: ServiceNow provides accessibility solutions for partners. Builder tools include features that help teams design more accessible interfaces and find and fix issues during the design process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/accessibility/builders-accessibility-features-and-updates.html
release: nofamily
topic_type: reference
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Product documentation for accessibility, Product accessibility]
---

# Builders' accessibility features and updates

ServiceNow provides accessibility solutions for partners. Builder tools include features that help teams design more accessible interfaces and find and fix issues during the design process.

## Find and fix issues feature in UI Builder

The Find and Fix Issues feature in UI Builder helps developers create accessible interfaces by providing real-time feedback and actionable guidance. This built-in diagnostic tool scans for common accessibility issues based on WCAG and Section 508 standards, flagging missing elements such as:

-   Alt text for images
-   ARIA labels for dynamic content
-   Other nuanced accessibility factors

This feature helps developers create more accessible experiences. However, some accessibility considerations require manual assessment, including:

-   Keyboard navigation functionality
-   Screen-reader experience optimization
-   Other nuanced accessibility factors

For a comprehensive understanding of how to use this feature effectively, refer to the detailed guide: [Find and fix issues in UI Builder](https://www.servicenow.com/docs/r/application-development/ui-builder/builder-assistant.html).

## Color contrast checker in Theme Builder

Customizing color palettes for UI components can impact the accessibility of your interface. Designers must verify that their color choices meet color contrast requirements so that they do not inadvertently create barriers for users with low vision or color blindness.

**The Accessibility Challenge:**

-   Color contrast: Users with visual impairments require strong contrast between UI components to navigate effectively.
-   Design oversight: Without proper tools, designers might overlook contrast issues, leading to accessibility errors.

**Theme Builder's Solution:**

Theme Builder includes a built-in **color contrast checker**. This feature:

-   Evaluates the contrast between UI components against established guidelines.
-   Alerts designers to potential issues by displaying an error next to components that fail to meet these standards.

The color contrast checker in Theme Builder helps designers verify that UI designs are accessible to a broader audience. Regularly checking for color contrast during the design process is a general guideline that enhances overall user experience.

See the following links for more information:

-   [Edit Components](https://www.servicenow.com/docs/r/platform-user-interface/tb-edit-components.html): Learn how to edit component and understand the color contrast error alerts.
-   [Adjust a component to meet accessibility standards](https://www.servicenow.com/docs/r/platform-user-interface/tb-adjust-component-wcag.html) : Discover how to use the color picker and other tools to select colors that meet accessibility standards.

## Custom fonts in Theme Builder

The Custom Font option in Theme Builder enables developers to upload a font to use on the interface.

The ability to upload custom fonts to your theme can help users with disabilities in several ways, including:

-   Improved readability: Custom fonts can be selected to enhance readability, making text easier to see, understand, and retain. This is beneficial for users with visual impairments, as clear letter forms reduce eye strain.
-   Support for cognitive differences: Custom fonts can address cognitive accessibility needs. For instance, users with dyslexia or Attention- Deficit/Hyperactivity Disorder \(ADHD\) may benefit from fonts that reduce reading strain and improve information processing.
-   Improved globalization support: Custom fonts tailored to specific languages improve the readability for non-Latin alphabets and help provide consistent, accessible user experiences across global audiences.

To learn more, see [Upload a custom font to your theme](https://www.servicenow.com/docs/r/platform-user-interface/upload-custom-font.html).

**Parent Topic:**[Product documentation for accessibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/nofamily/markdown/accessibility/available-accessibility-product-documentation.md)

