---
title: Key terms referred in Web Embeddables
description: The following are the key terms referred in Web Embeddables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Web Embeddables reference, Reference, Customer Service Management]
---

# Key terms referred in Web Embeddables

The following are the key terms referred in Web Embeddables.

<table id="table_wkj_blc_25b"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Global code

</td><td>

Global code is a common script for all the ServiceNow components. It enables you to define component themes, base URLs, authentication callbacks, and locale settings before embedding components onto your website. Additionally, it optimizes component performance by pre-caching the resources required for the components. You must add global code before adding component code onto your website hosting ServiceNow web embeddable components verifying a consistent look and feel, secure communication, and proper localization. Without including this script, your components don't render correctly or function as expected, potentially leading to issues with your user experience and functionality.

</td></tr><tr><td>

Component code

</td><td>

Component code is a component-specific script designed for each component that enables you to define how each component behaves, appears, and integrates within your webpage. The code contains all the necessary logic and functions to ensure the integration and operation of the components in your website’s ecosystem. Facilitating the proper display and interaction of the component but also managing dependencies with other components.

**Note:** The component code is unique for all ServiceNow components.

</td></tr><tr><td>

CORS \(Cross-Origin Resource Sharing\) rules

</td><td>

CORS rules are a security mechanism in web browsers designed to control how resources on your webpages are accessed from different domains. This mechanism helps protect your data and resources from unauthorized access. By configuring CORS rules, you can specify and enforce access policies verifying that your embedded components can securely communicate with ServiceNow components. It is crucial for maintaining the integrity and security of your interactions on the website.

</td></tr><tr><td>

Event handler

</td><td>

An event handler lets you configure actions, components, or declarative actions on your website. For example, you can map an event to your component to display an alert notification when the user selects any button on the confirmation message, or you can add an event handler to respond to a record creation failure.

</td></tr><tr><td>

Static preview

</td><td>

The static preview provides a visual representation of your component when a live preview is unavailable. It enables you to understand the component layout and design. However, with static preview enabled, any changes made to global or component properties aren't reflected in the preview in real time. This feature is useful for reviewing components in scenarios where dynamic rendering isn’t available. The Static preview is not available for custom and Data visualization component.

</td></tr><tr><td>

Component instance

</td><td>

Enables administrator to save and retrieve configuration of a component embedded on a specific location on the third-party website. Component instances can be renamed, duplicated, and rearranged within the group or across groups.

</td></tr><tr><td>

Group

</td><td>

Enables administrator to model their third-party website structure such as pages or sections. After recreating the website’s structure, administrator can add component instances within the group.

</td></tr><tr><td>

Module

</td><td>

A module represents a website with a collection of pages or a section using groups and a collection of components instances embedded on the website. The theme for component instances, external domain URL for CORS, and custom ServiceNow domain for base URL are derived from module meta data.

</td></tr></tbody>
</table>