---
title: Rich Text Label
description: This variable displays a formatted label on a catalog item form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/rich-text-label.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Rich Text Label

This variable displays a formatted label on a catalog item form.

In the TinyMCE rich text editor, you can format the label and add images or links. This variable supports the HTML tags.

**Note:**

-   You can make this variable visible using catalog client scripts and catalog UI policies.
-   You cannot cascade this variable in an order guide.
-   You cannot set this variable as mandatory.
-   In the Automated Test Framework, this variable is only supported in the Variable State Validation step to check the visibility.
-   This variable is not supported in the following:
    -   Variable summarizer
    -   Multi-row variable set
    -   Condition builders and reports
-   You cannot specify the following for this variable:
    -   Help text and instructions
    -   Tool tip
    -   Permissions
    -   Variable width
    -   Example text
-   The g\_form.setValue\(\), g\_form.setReadOnly\(\), and g\_form.setMandatory\(\) APIs are not supported in catalog client scripts. Only the g\_form.setVisible\(\) API is supported.

\[Omitted image "RichTextVariable.png"\] Alt text: The Rich Text Label variable

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Check box]()

[Container start, container split, and container end]()

[Date, Date and time, and Duration]()

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/email.md)

[HTML]()

[IP Address]()

[Label]()

[List collector]()

[Lookup multiple choice]()

[Lookup select box]()

[Custom and Custom with label]()

[Masked]()

[Multi-line text]()

[Multiple choice]()

[Numeric scale]()

[Reference]()

[Requested for]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

