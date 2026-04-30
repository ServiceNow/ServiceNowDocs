---
title: Add content controls in a Microsoft Word document
description: As a legal contract configurator, prepare a Microsoft Word document that you want to import as a contract template by marking the content with content controls so it can be efficiently parsed and reused.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure legal contract templates of type Microsoft Word, Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add content controls in a Microsoft Word document

As a legal contract configurator, prepare a Microsoft Word document that you want to import as a contract template by marking the content with content controls so it can be efficiently parsed and reused.

## Before you begin

Ensure that you are on a Windows system to add content controls in a Microsoft Word document.

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  In Microsoft Word, open the document that you want to import as a contract template.

2.  Display the **Developer** tab in Microsoft Word.

    For more information, see the [Show the Developer tab](https://support.microsoft.com/en-us/office/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) topic in the Microsoft Office 365 documentation.

3.  Select the content to be tagged.

4.  Select **Plain Text Content Control** from the **Developer** tab.

5.  Select the **Properties** option from the **Developer** tab.

6.  In the **Content Control Properties** dialog box, enter a title for the content control.

7.  Enter a tag value.

    **Note:**

    -   The tag names are not case sensitive. If there are two tag names as field\_COMPANY and field\_company, both will be treated same.
    -   The maximum character limit for the tag is 200.
    Tag names contain a prefix with the content control type.

    |Content control type|Description|
    |--------------------|-----------|
    |field\_|Indicates metadata.|
    |signature\_|Indicates a signature.|
    |sign\_date\_|Indicates the signing date.|

    For example, Microsoft Outlook Add-In for Legal Service Delivery If you are adding a metadata for company name, you would name the tag **field\_company**.

    ![Content control example](../image/lsc-add-ctrl-field.png)

8.  Select **OK**.


**Parent Topic:**[Configure legal contract templates of type Microsoft Word](lsc-configure-ct-msword.md)

**Related topics**  


[Create a Microsoft Word legal contract template](lsc-create-ct-msword.md)

[Create and configure participants for legal contract template](lsc-add-config-participants-msword.md)

[Update contract template mappings for legal contract template](lsc-template-map-msword.md)

[Publish a contract template](lsc-publish-word-template.md)

