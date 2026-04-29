---
title: Extension points
description: Use extension points to extend the functionality of an application without altering the original application code. Recommendation contexts use extension points to enable additional functionality while configuring the recommendation contexts or templates.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recommendation contexts and templates, Common GRC features, Governance, Risk, and Compliance]
---

# Extension points

Use extension points to extend the functionality of an application without altering the original application code. Recommendation contexts use extension points to enable additional functionality while configuring the recommendation contexts or templates.

## Extension points overview

As a developer, you can use pre-existing extension points or add extension points as you develop custom applications in your instance. By using extension points in your recommendation contexts, you can integrate customizations without altering the core components in the application code. Extension points can avoid custom code interactions from breaking, which often occurs after an upgrade if you directly embed the custom code into the application code.

Extension points that are embedded in the application code act as out-points, where data passes to the custom code, and as in-points that handle the returned results. When creating an application, the returned data or objects must conform to the requirements that the developers define for the extension point. For example, you can use the base extension point RCM\_Recommendation\_ExtensionPoint to configure recommendation contexts or templates for a regulatory alert.

## Types of extension points

You can create extension points to process the custom code that uses the following types of artifacts:

-   **Scripted extension points**

    Extension points in the server-side script includes that store JavaScript functions and object classes.

-   **UI extension points**

    Extension points that are used in server-side UI macros such as HTML extensions.

-   **Client extension points**

    Extension points that are used in client-side UI scripting, typically for modifying forms.


For more information about extension points, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/bundle/australia-api-reference/page/build/applications/concept/extension-points.html).

**Parent Topic:**[Recommendation contexts and templates](recommendation-contexts.md)

