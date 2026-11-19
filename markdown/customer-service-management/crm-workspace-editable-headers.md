---
title: CRM Workspace editable record headers
description: Customer service agents can edit the short description \(primary field\) of a record directly from the record header field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/crm-workspace-editable-headers.html
release: brazil
topic_type: reference
last_updated: "2026-11-16"
reading_time_minutes: 2
breadcrumb: [Form features, CRM Workspace features, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CRM Workspace editable record headers

Customer service agents can edit the short description \(primary field\) of a record directly from the record header field.

The editable record header feature includes the following benefits:

-   The system validates the text entered in the record header field.
-   The **Short description** field \(primary field\) automatically updates with the changes made in the record header field.
-   Changes to the record header field are saved when the agent saves the record.
-   Empty record header fields display placeholder text. For example, default placeholder text such as **Enter short description here** is displayed for new record forms.
-   The text in the record header field is truncated if it is longer than the field width. Hovering over the field displays the full text.
-   Editing permissions for the record header field are restricted to authorized agent roles.

**Note:** The record header is not editable if the form field used as the record header is either read-only or not present on the form.

To edit the text, simply select the record header field and make the changes.

This feature is available on the following CRM Workspace record pages:

-   [Front-line case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-front-line-case-page.md)
-   [CSM Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-interaction-record-page.md)
-   [CSM default record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-default-record-page.md)
-   [CSM voice interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-native-voice-record-page.md)
-   [CSM centered chat interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-centered-chat-interaction-page.md)
-   [Email Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-email-interaction-record-page.md)

Suggestions for using the editable record header feature:

-   Use only static text fields such as **Short description** or **Subject** as the editable record header field.
-   Don't re-use the placeholder text as the value in the record header field as the placeholder text indicates that the field is empty.

    **Note:** If the placeholder text is used as the value in the record header field, the agent must double-click the record header field to change the text.


