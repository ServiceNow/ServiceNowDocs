---
title: CRM Workspace visual field indicators
description: Use visual indicators in CRM Workspace such as icons and background colors to indicate form fields with unsaved changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/crm-workspace-visual-field-indicators.html
release: brazil
topic_type: reference
last_updated: "2026-11-16"
reading_time_minutes: 1
breadcrumb: [Form features, CRM Workspace features, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CRM Workspace visual field indicators

Use visual indicators in CRM Workspace such as icons and background colors to indicate form fields with unsaved changes.

When visual indicators are enabled, customer service agents see the following indicators on record forms:

-   Dot icons appear next to the field labels for updated fields.
-   Background colors change for updated fields.
-   Tooltips identify each updated field.

Field updates include manual changes made by the agent, by the application of a template, or automatic updates made by AI. These visual indicators are removed when the agent saves the form.

This feature is available for the following CRM Workspace [record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-config-workspace-record-pages.md):

-   Front-line case page
-   CSM default record page
-   Email interaction record page
-   CSM voice interaction record page
-   CSM Interaction record page
-   CSM centered chat interaction record page

## Enabling visual field indicators

Users with the administrator role can enable the background colors along with a dot icon to indicate fields with unsaved changes. The workspace-level property **enableBgColorForUnsavedFieldIndicator** controls these indicators. This property is set to true by default.

To set this property:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experience**.
2.  Select **CRM Workspace**.
3.  In the UX Page Properties related list, select **enableBgColorForUnsavedFieldIndicator**.
4.  Update the value in the **Value** field.
5.  Select **Update**.

