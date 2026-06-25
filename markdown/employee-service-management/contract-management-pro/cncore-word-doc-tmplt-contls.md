---
title: Add content controls in a Microsoft Word document
description: As a contract configurator, prepare a Microsoft Word document that you want to import as a contract template by marking the content with content controls so it can be efficiently parsed and reused.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-word-doc-tmplt-contls.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create contract template by manually adding content controls, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add content controls in a Microsoft Word document

As a contract configurator, prepare a Microsoft Word document that you want to import as a contract template by marking the content with content controls so it can be efficiently parsed and reused.

## Before you begin

Ensure that you are on a Windows system to add content controls in a Microsoft Word document.

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  In Microsoft Word, open the document that you want to import as a contract template.

2.  On the Microsoft Word Home ribbon, select the Show/Hide formatting marks icon \(\[Omitted image "lsd-word-formatting-icon.png"\] Alt text: Show/Hide formatting marks icon\) to see the formatting symbols.

3.  Display the **Developer** tab in Microsoft Word.

    For more information, see the [Show the Developer tab](https://support.microsoft.com/en-us/office/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) topic in the Microsoft Office 365 documentation.

4.  Select the content to be tagged.

5.  Select **Plain Text Content Control** from the **Developer** tab.

    \[Omitted image "lsd-content-control-eg.png"\] Alt text: Content control example

6.  Select the **Properties** option from the **Developer** tab.

7.  In the **Content Control Properties** dialog box, enter a title for the content control.

8.  Enter a tag value.

    **Note:**

    -   The tag names are not case sensitive. If there are two tag names as clause\_PURPOSE and clause\_purpose, both will be treated same.
    -   The maximum character limit for the tag is 200.
    -   When inserting content controls for signatures or signatories, ensure the font color of the tagged text matches the document’s background color.
    Tag names contain a prefix with the content control type.

    |Content control type|Description|
    |--------------------|-----------|
    |field\_|Indicates metadata.|
    |clause\_|Indicates a clause.|
    |signature\_|Indicates a signature.|
    |sign\_date\_|Indicates the signing date.|
    |signatory\_name|Indicates the name of the signatory.|
    |signatory\_email|Indicates the email of the signatory.|
    |signatory\_title|Indicates the title of the signatory.|

9.  Select **OK**.


**Parent Topic:**[Create contract template by manually adding content controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-setup-ct-manual.md)

**Related topics**  


[Create a contract template]()

[Create and configure participants]()

[Classify and map imported clauses]()

[Update contract template mappings]()

