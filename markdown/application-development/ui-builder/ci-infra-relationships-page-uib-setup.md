---
title: CI infrastructure relationships page template setup
description: The CI infrastructure relationships page tracks the relationships between configuration items \(CI\) and provides links to drill down into the affected CIs in each class.Configure the reusable CI infrastructure relationships page template in your experience with different values and behaviors than those provided by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/ci-infra-relationships-page-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# CI infrastructure relationships page template setup

The CI infrastructure relationships page tracks the relationships between configuration items \(CI\) and provides links to drill down into the affected CIs in each class.

Pages are built in UI Builder using a template. For instructions on accessing UIB and selecting the page template you want, see [Create a page from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/reuse-page-definitions.md) or [Create a page from a legacy template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/legacy-templates.md).

## How to use the template

Create a new page from this template in UI Builder, and choose one of the following options:

-   **Use the original template**: References the template in your page. When the template is updated for a new release, your page gets the updates automatically. This selection permits limited customizations but is the safest choice.
-   **Copy template contents**: Allows you to change the property values for the components used in the page. When you copy a template, you don't get any of the changes when the template is automatically updated for a new release.

## Renaming components

You can rename components in the content tree to suit your use case. For details about editing the content tree, see [UI Builder quick start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/ui-builder-quick-start.md).

## Page layout

For instructions on creating and editing page layouts, see [Layouts in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-layouts.md).

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## CI infrastructure relationships page template properties

Configure the reusable CI infrastructure relationships page template in your experience with different values and behaviors than those provided by default.

### Before you begin

You can configure the properties for the this page in the UX Applications \[sys\_ux\_page\_registry\] table.

Role required: workspace\_admin or ui\_builder\_admin

### Procedure

1.  Navigate to **Next Experience Framework** &gt; **Experiences**.

2.  In the list of UX Applications, select the title of the experience that uses the page template.

3.  Select the UX Page Properties related list to view the properties included with the page template.

    You can select a property to edit or create a new property for your experience.

4.  To create a new page property:

    1.  Navigate to **sys\_ux\_page\_property.list**.
    2.  In the list of page properties, select **New**.
    3.  In the page property record, select an existing page \(UX application title\) for the property.
    4.  Create a unique name for the property and assign it a value.
    5.  Select **Submit**.

        Your new property appears in the UX Page Properties related list in the UX Application record for the page you selected.


