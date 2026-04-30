---
title: Modify the banner
description: The banner is displayed at the top of the page and is rendered using certain system properties.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a company profile, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Modify the banner

The banner is displayed at the top of the page and is rendered using certain system properties.

**Note:** From the San Diego release on, configure banner announcements instead of updating **glide.product.description**, which is not used when Next Experience is enabled.

For more information, see [Configure Next Experience banner announcements](next-experience-banner-announcements.md#).

-   **glide.product.image**
-   &lt;div&gt;**glide.product.name**&lt;/div&gt;
-   &lt;div&gt;**glide.product.description**&lt;/div&gt;

The DIV that contains the **glide.product.name** property is only shown if the property contains a value, otherwise, it is not used when rendering the banner. Also, the property **glide.banner.image.title** controls the tooltip that appears when the cursor is over the banner.

**Note:** The My Company record overrides the properties.

![Classic environment banner.](../image/Banner.png "Banner")

## Window title

These properties are used to set the window title as follows:

**glide.product.name** **glide.product.description**

If **glide.product.name** is blank, then the ServiceNow name is used as the product name for the window title.

## My Company

The banner text and banner image defined for the Company that a user is assigned to may be used to override the **glide.product.image** and **glide.product.description**. The banner text, if specified, is used instead of the **glide.product.description** property. The banner image, if specified, is used instead of the **glide.product.image** property.

**Parent Topic:**[Create a company profile](../task/t_CreateACompanyProfile.md)

**Related topics**  


[Banner logo link](c_CustomizeTheBannerLogoLink.md)

[Customize the banner logo in Core UI](../task/t_CustomizeTheLogoInSysProps.md)

[Customize the favicon](../task/customize-favicon.md)

[Examples of how to modify the banner](c_ExamplesOfHowToModifyTheBanner.md)

