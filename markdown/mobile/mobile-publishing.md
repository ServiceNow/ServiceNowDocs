---
title: Publish mobile apps with custom branding
description: The ServiceNow Mobile Publishing application enables you to publish secure and branded mobile applications. These mobile apps use your unique company identity and management method.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Publish mobile apps with custom branding

The ServiceNow® Mobile Publishing application enables you to publish secure and branded mobile applications. These mobile apps use your unique company identity and management method.

ServiceNow offers the following ways to customize your mobile apps:

-   Branding: Determines what users see before they reach the login screen.
-   Theming: Determines what users see after they log in.

Mobile Publishing enables you to brand your mobile apps. You can use Mobile Publishing to create a visually distinct version of ServiceNow mobile apps with custom branding that reflects your unique company identity. Configure each of your mobile apps with a unique name, splash screen, icon, Mobile Device Management \(MDM\) vendor, and colors.

For information about using theming to further customize your apps, see:

-   [Next Experience theming for mobile](explore-ne-theming.md)
-   [Legacy mobile theming](sg-themes.md)

In addition to branding and theming your mobile apps, you can also customize app behavior to make them more efficient for your end-users to use. For example, you can request a custom branded mobile app and configure an auto-populated URL so your end-users don't need to type the instance URL during login. This can be configured in the **Login management** section of the **Request a new app** form. For more information, see the [Request, test, and publish a branded mobile app](request-test-pub-branded-mob-app.md) section that contains instructions for requesting custom branded apps for both the iOS and the Android platforms.

For more information about the considerations for using Mobile Publishing and configuring it, see [Mobile Publishing resources](mobile-publishing-resources.md). For information about why your company might want to use Mobile Publishing, see [Mobile Publishing use cases](mobile-publishing-use-cases.md).

**Note:** Mobile Publishing is supported on both production and sub-production ServiceNow instances.

The ServiceNow publishing program complies with the suggested practices from Google and Apple for branded app releases. The program gives you a guided path to achieve your branding goals.

## Licensing

Mobile Publishing is a paid plugin. It is included in the Pro, Enterprise, and App Engine subscription levels \(SKU's\) of ServiceNow. Alternatively, you can purchase the plugin on the ServiceNow Store and add it to your ServiceNow subscription. Navigate to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), log in with your credentials, and then search for `mobile publishing`.

## Custom-type mobile apps

Use Mobile Publishing to brand standard Now Mobile and Mobile Agent apps that are part of the ServiceNow Mobile Platform. If you need additional client app types other than Now Mobile and Mobile Agent, you can create custom app types that have unique mobile client app names.

For more information about custom mobile apps, see [Create custom-type mobile apps with Mobile Publishing](mob-pub-about-custom-apps.md).

For more information about the integration between Mobile Publishing and Mobile App Builder, see [Mobile App Builder](mab-concept.md).

## Manage your custom-branded apps

Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps** in your instance. Do any of the following \(refer to the numbered call-outs in the below image\):

1.  View your recent app requests. A maximum of nine builds can be tracked on this page.
2.  Request a new branded app by selecting **Request a new app**.
3.  Get information about what you need \(prerequisites\) to request different apps and associated distribution types.
4.  Watch a video that guides you through the process of requesting a custom branded app and shows you how the third-party tools are used to populate mandatory fields on the request form.
5.  Access helpful resources and FAQs to get further help.

![Mobile Publishing main page](../image/mob-pub-overview-tab-page-full.png "Mobile Publishing overview tab page")

Scroll down to view the brand assets guide panel \(refer to the below image\), which supplies guidelines to help you create a consistent brand experience for iOS and Android apps.

![Mobile Publishing brand assets guide panel](../image/mob-pub-overview-tab-brand-assets-guide-panel.png "Mobile Publishing brand assets guide panel")

## Request custom-branded apps with the build request form

The build request form has sections that you can navigate between to make sure your build request suits your organization's requirements \(refer to the numbered call-outs in the below image\):

1.  Use the **Back** and **Next** buttons at the bottom of the form to access build options or to revisit options you've already selected so you can make any needed corrections.
2.  View the right panel to get help from product documentation and FAQs.

    **Note:** Hover over the FAQs to see the full question and to expand the list to see the answers.


![Mobile Publishing build request form](../image/mob-pub-build-request-form.png "Mobile Publishing build request form")

## View custom branded app builds and check build progress

\(Refer to the below image\):

![Mobile Publishing history tab full page](../image/mob-pub-history-tab-page.png "Mobile Publishing history tab page")

Select one of the build cards on the history tab page to drill down for details about the app build \(refer to the numbered call-outs in the below image\):

1.  View who requested the app and their email contact information.
2.  Get details about the app type, distribution type \(private or public\), what mobile application management \(MAM\) vendor the app uses, and its operating system.

![Mobile Publishing build details page](../image/mob-pub-history-tab-request-details-panel.png "Mobile Publishing build details page")

-   **[Prerequisites for Mobile Publishing](mobile-publishing-prerequisites.md)**  
Before submitting your first branded app request with Mobile Publishing, it's important to set up some prerequisite tools.
-   **[Distributing your mobile app](mobile-distribution.md)**  
Learn about making your mobile apps available for download to Android and iOS devices.
-   **[Request, test, and publish a branded mobile app](request-test-pub-branded-mob-app.md)**  
Publish secure custom mobile apps with your unique company identity by requesting branded versions of ServiceNow mobile apps.
-   **[Building and configuring in branded mobile apps](build-configure-branded.md)**  
Learn about configuring push notifications for branded mobile apps.
-   **[Mobile Publishing resources](mobile-publishing-resources.md)**  
Here are some additional resources to help you plan and publish branded mobile applications.
-   **[Mobile Publishing use cases](mobile-publishing-use-cases.md)**  
Here are several reasons to use Mobile Publishing to brand the mobile apps of your company.

