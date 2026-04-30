---
title: Request Anglepoint's IBM Licensing for Software Asset Management application
description: If you are integrating the Software Asset Management publisher pack for IBM with Anglepoint, request Anglepoint's IBM Licensing for Software Asset Management application from the ServiceNow Store. This application extends the base Software Asset Management File Names \[samp\_file\_name\], File Maps \[samp\_file\_map\], and File Sets \[samp\_file\_set\] tables so that you can store IBM software information from Anglepoint.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up an IASP integration, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Request Anglepoint's IBM Licensing for Software Asset Management application

If you are integrating the Software Asset Management publisher pack for IBM with Anglepoint, request Anglepoint's IBM Licensing for Software Asset Management application from the ServiceNow® Store. This application extends the base Software Asset Management File Names \[samp\_file\_name\], File Maps \[samp\_file\_map\], and File Sets \[samp\_file\_set\] tables so that you can store IBM software information from Anglepoint.

## Before you begin

Role required: admin

## About this task

The IBM Licensing for Software Asset Management application contains table dictionaries that extend the base File Names \[samp\_file\_name\], File Maps \[samp\_file\_map\], and File Sets \[samp\_file\_set\] tables as follows:

|Base table|Extended table|
|----------|--------------|
|File Names \[samp\_file\_name\]|Anglepoint File Names \[samp\_anglepoint\_file\_name\]|
|File Maps \[samp\_file\_map\]|Anglepoint File Maps \[samp\_anglepoint\_file\_map\]|
|File Sets \[samp\_file\_set\]|Anglepoint File Sets \[samp\_anglepoint\_file\_set\]|

The extended tables store software information from the IBM software discovery catalog that is maintained by Anglepoint. You can add this software information to these tables by downloading the IBM software discovery catalog from the Anglepoint Elevate platform and then uploading it to your ServiceNow instance. Discovery tools, such as the ServiceNow® Discovery application, can then use this software information to identify the IBM software that is discovered in your environment. See [Upload the IBM software discovery catalog to your ServiceNow instance](upload-anglepoint-software-discovery-catalog.md) for more information on the IBM software discovery catalog.

## Procedure

1.  From a web browser, go to the [ServiceNow Store](https://store.servicenow.com/).

2.  Log in using your HI credentials.

3.  In the search bar, enter `IBM Licensing for Software Asset Management` and then select **Search**.

4.  Select the result called **IBM Licensing for Software Asset Management**.

5.  On the IBM Licensing for Software Asset Management page, select **Request Install**.

    The ServiceNow Request for App Installation - IBM Licensing for Software Asset Management dialog box opens.

6.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Instance Name|Name of the instance on which you want to install the application. After you enter the instance name, select **Validate Instance** to verify that the instance exists.|
    |Reason for request|Reason for requesting the application.|

7.  Select **Request**.

8.  Select **Close**.


## Result

If your request is approved, you will receive an email with detailed instructions on how to install the application.

## What to do next

Install the application according to the instructions in the email.

**Parent Topic:**[Setting up an IBM Authorized SAM Provider \(IASP\) integration](../concept/setting-up-anglepoint-integration.md)

