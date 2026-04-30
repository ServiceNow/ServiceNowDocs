---
title: Upload the IBM software discovery catalog to your ServiceNow instance
description: Upload the IBM software discovery catalog to your ServiceNow instance so that discovery tools, such as the ServiceNow Discovery application, can identify the IBM software that is discovered in your environment.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up an IASP integration, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Upload the IBM software discovery catalog to your ServiceNow instance

Upload the IBM software discovery catalog to your ServiceNow instance so that discovery tools, such as the ServiceNow® Discovery application, can identify the IBM software that is discovered in your environment.

## Before you begin

Role required: sam\_admin

## About this task

The IBM software discovery catalog is a centralized repository of IBM software information that discovery tools can use to identify discovered IBM software. This catalog is maintained separately by each authorized Software Asset Management provider.

## Procedure

1.  Download the IBM software discovery catalog from the authorized Software Asset Management provider that you are integrating with.

2.  Upload the catalog to your ServiceNow instance.

    1.  From your ServiceNow instance, navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Import IBM Content**.

    2.  On the Manage Software Library form, select **Attach Content File**.

        The Attachments dialog box opens.

    3.  In the dialog box, select **Choose file** to search for and select the IBM software discovery catalog that you downloaded from the Anglepoint Elevate platform.

    4.  Close the dialog box to return to the Manage Software Library form.

    5.  Select **Run Import**.


## Result

If you are integrating with Anglepoint, all IBM software information that is included in the catalog is stored in the following Software Asset Management tables:

-   Anglepoint File Names \[samp\_anglepoint\_file\_name\]
-   Anglepoint File Maps \[samp\_anglepoint\_file\_map\]
-   Anglepoint File Sets \[samp\_anglepoint\_file\_set\]

**Note:** These tables are extensions of the base File Names \[samp\_file\_name\], File Maps \[samp\_file\_map\], and File Sets \[samp\_file\_set\] tables. To extend the base tables, you must request and install Anglepoint's IBM Licensing for Software Asset Management application. See [Request Anglepoint's IBM Licensing for Software Asset Management application](request-anglepoint-application.md) for detailed instructions.

**Parent Topic:**[Setting up an IBM Authorized SAM Provider \(IASP\) integration](../concept/setting-up-anglepoint-integration.md)

