---
title: Create a company profile
description: To customize the ServiceNow instance for your company, you can enter information such as contact phone numbers, street address, and additional notes. You can also customize the company logo and banner text your end users see at the top of each page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a company profile

To customize the ServiceNow instance for your company, you can enter information such as contact phone numbers, street address, and additional notes. You can also customize the company logo and banner text your end users see at the top of each page.

## Before you begin

Role required: admin

## About this task

Much of the company information that you enter is reference information that administrators can view. All users see the company logo and banner text. To see all company information, verify that you are in the **My Company** view.

![Select the My Company view](../image/MyCompanyView.png "My Company view selection")

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **My Company**.

2.  To change the banner text, update the **Banner text** field.

3.  Select the **Primary** check box to indicate if this company is the primary company.

    If needed, [configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to add the **Primary** check box. Designate only one company in your system as the primary company.

4.  To upload your company logo, select **Click to add** or **Update** beside **UI16 Banner Image**.

    If you leave the banner image blank in Core UI \(UI16\), the system uses the image used in **System Properties** &gt; **Basic Configuration** &gt; **Banner image** \[glide.product.image\] as the default.

5.  Click **Choose file** and select the file, and then click **OK**.

    To use an image URL instead of a file on your hard drive, enter the URL in the file upload window.

6.  Complete the form with remaining company information.

7.  Click **Update**.


-   **[Banner logo link](../concept/c_CustomizeTheBannerLogoLink.md)**  
Properties are available to control the URL and target frame used when clicking the banner logo.
-   **[Customize the banner logo in Core UI](t_CustomizeTheLogoInSysProps.md)**  
Use the **glide.product.image** and **glide.product.description** properties to change the banner logo and description in Core UI.
-   **[Customize the favicon](customize-favicon.md)**  
Use the **glide.product.icon** property to change the icon that appears in bookmarks and the browser address bar.
-   **[Examples of how to modify the banner](../concept/c_ExamplesOfHowToModifyTheBanner.md)**  
There are various ways that you can modify the banner on your instances.
-   **[Modify the banner](../concept/c_ModifyTheBanner.md)**  
The banner is displayed at the top of the page and is rendered using certain system properties.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

