---
title: Rich Text Label
description: This variable displays a formatted label on a catalog item form.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-20"
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

![The Rich Text Label variable](../image/RichTextVariable.png "Rich Text Label variable")

**Parent Topic:**[Types of service catalog variables](r_VariableTypes.md)

**Related topics**  


[Attachment](attachment.md)

[Break](break.md)

[Check box](check-box.md)

[Container start, container split, and container end](contain-start-split-end.md)

[Date, Date and time, and Duration](date.md)

[Email](email.md)

[HTML](html.md)

[IP Address](ip-address.md)

[Label](label.md)

[List collector](list-collector.md)

[Lookup multiple choice](lookup-multiple-choice.md)

[Lookup select box](lookup-select-box.md)

[Custom and Custom with label](custom.md)

[Masked](masked.md)

[Multi-line text](multi-line.md)

[Multiple choice](multiple-choice.md)

[Numeric scale](numeric-scale.md)

[Reference](reference.md)

[Requested for](requested-for.md)

[Select box](select-box.md)

[Single-line text](single-line-text.md)

[UI page](ui-page.md)

[URL](url.md)

[Wide single-line text](wide-single-line-text.md)

[Yes/No](yes-no.md)

[Variable support in various channels](variables-availability.md)

