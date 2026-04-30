---
title: Configure the Export to PowerPoint add-in for Microsoft PowerPoint
description: Configure the Export to PowerPoint add-in in your Microsoft PowerPoint to interact with your instance and fetch the data required to generate and download your project status reports.
locale: en-US
release: xanadu
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Configure the Export to PowerPoint add-in for Microsoft PowerPoint

Configure the Export to PowerPoint add-in in your Microsoft PowerPoint to interact with your instance and fetch the data required to generate and download your project status reports.

## Before you begin

-   Role required: sn\_ppt\_export.ppt\_admin or sn\_ppt\_export.ppt\_user.
-   The Export to PowerPoint add-in must be deployed to your Microsoft PowerPoint. If the add-in icon does not appear on the Home tab, verify the following.
    1.  [Download the add-in manifest file](download-manifest-export-to-ppt.md) from your ServiceNow instance.
    2.  Contact your Microsoft Office 365 administrator to deploy the manifest using the Microsoft 365 admin center \(**Settings** &gt; **Integrated apps** &gt; **Upload custom apps**\).
    3.  After deployment, restart Microsoft PowerPoint and verify the ServiceNow add-in icon appears on the Home tab.
-   For the Export to PowerPoint plugin configuration on your instance, see Configure the Export to PPT plugin.

**Tip:**

If you do not see the add-in icon after deployment, check **Insert** &gt; **My Add-ins** in Microsoft PowerPoint to verify the add-in is installed. You may need to select it manually to add it to your ribbon.

## Procedure

1.  Open your Microsoft PowerPoint application and select the ServiceNow add-in icon \(![ServiceNow Export to PowerPoint add-in.](../image/icon-servicenow-addin.png)\) on the **Home** tab.

    A panel appears with a login option to access your ServiceNow instance.

2.  Select **Log in**.

3.  Enter your ServiceNow instance credentials and select **Log in**.

    A prompt requesting access to your instance with details such as the instance name is displayed.

4.  Check your instance details and select **Allow**.


## Result

The landing page of the add-in appears as the right panel.

![Export to PowerPoint add-in landing page.](../image/icon-ppt-addin-landing-page.png)

**Note:** For more information about the additional configuration steps required to enable the Export to PowerPoint add-in for the browser version of Microsoft PowerPoint, see the [KB1171422](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1171422) article in the Now Support Knowledge Base.

## What to do next

[Create a Microsoft PowerPoint template](create-ppt-template.md).

**Parent Topic:**[Configuring Export to PowerPoint](../concept/configure-export-to-ppt.md)

