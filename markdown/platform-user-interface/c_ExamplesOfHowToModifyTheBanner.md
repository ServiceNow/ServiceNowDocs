---
title: Examples of how to modify the banner
description: There are various ways that you can modify the banner on your instances.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a company profile, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Examples of how to modify the banner

There are various ways that you can modify the banner on your instances.

**Note:** From the San Diego release on, configure banner announcements instead of updating **glide.product.description**. For more information, see [Configure Next Experience banner announcements](next-experience-banner-announcements.md#).

## Label multiple instances differently

-   On all instances, leave **glide.product.description** &lt;blank&gt;
-   On PROD instance, set **glide.product.name** to &lt;My Company&gt;
-   On DEV instance, set **glide.product.name** to &lt;My Company - DEV&gt;

## Control the window title

Since the window title is composed of **glide.product.name** and **glide.product.description**, the following gives you complete control over the banner and the window title.

-   **glide.product.name** set to &lt;Window Title that you want&gt;
-   **glide.product.name.style** set to &lt;display: none&gt;
-   **glide.product.description** set to &lt;blank&gt;

The company record **Banner Image** and **Banner Text** are used to set the banner image and text since the company banner text is not used in the window title.

## Use HTML in the banner text

-   **glide.product.name** set to &lt;My Company&gt;
-   **glide.product.name.style** set to &lt;display: none&gt;
-   **glide.product.description** set to &lt;Some text &lt;a href="some\_url"&gt;Click here&lt;/a&gt;&gt;

## Position banner text over the banner image

-   **glide.product.name** set to &lt;My Company&gt;
-   **glide.product.name.style** set to &lt;display: none&gt;
-   **glide.product.image** set to &lt;your company logo.gif&gt;
-   **glide.product.description** set to &lt;Some text for the description&gt;
-   **glide.product.description.style** set to &lt;position:absolute; top:5px; left:100px&gt; \(position values may vary based on specified needs\)

## Apply a background image to the banner

Often corporate guidelines require more in-depth branding of the ServiceNow interface. Using the tiling technique, you can modify your logo image to have a transparent background, so that you can apply another image to the banner beneath the logo.

Upload an image to the image manager and then create a new property named **css.banner.background.image**, so that you can call the image. The value should look like this.

**css.banner.background.image** value url\('./images/MasterBG.jpgx'\)

## Write CSS rules that apply this change

```
/** BACKGROUND - These properties allow you use to add a background tile to the header of the instance  ***************************/
TD.bannerLeft,TD.bannerCenter,TD.bannerRight, TR#banner_row{background-color: ${banner.background.color};
background-image: ${banner.background.image};
background-position: ${banner.background.position};
background-repeat: ${banner.background.repeat};}
```

**Note:** The banner image and banner text associated with the primary company or specific companies may be used instead of the **glide.product.image** and **glide.product.description** properties to get the same effect.

**Parent Topic:**[Create a company profile](../task/t_CreateACompanyProfile.md)

**Related topics**  


[Banner logo link](c_CustomizeTheBannerLogoLink.md)

[Customize the banner logo in Core UI](../task/t_CustomizeTheLogoInSysProps.md)

[Customize the favicon](../task/customize-favicon.md)

[Modify the banner](c_ModifyTheBanner.md)

