---
title: Update a branded app
description: Request and publish an update to a ServiceNow mobile app that has been branded with your unique company identity. Updates can only be requested for approved, completed builds of branded apps.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Update a branded app

Request and publish an update to a ServiceNow® mobile app that has been branded with your unique company identity. Updates can only be requested for approved, completed builds of branded apps.

## Before you begin

Role required: admin

## About this task

Mobile Publishing enables you to request an updated version of your branded iOS or Android app that you can distribute publicly or privately. You can request an update for the following branded app options:

-   New version of the ServiceNow mobile app.
-   Requester contact information such as first name, family name, and email address.
-   Change whether you want to use your custom End-User License Agreement \(EULA\) and privacy policy or the default ServiceNow EULA and privacy policy.
-   For iOS apps that use private distribution, you can add or delete testers for [TestFlight](https://developer.apple.com/testflight/) notifications.

**Important:** Only the above information can be changed on completed builds of branded apps. If you must change any other options, you must request a new branded app with Mobile Publishing.

## Procedure

1.  Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps**.

2.  In **Your recent app requests** section of the page, select the completed branded mobile app build that you want to update.

3.  On the **Request details** page for the branded mobile app, select **Duplicate**.

    The **Review and submit** page appears for the branded mobile app.

4.  On the Review and submit form, fill in the following fields to update the app.

<table id="table_dww_t13_mrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Your contact info

</td><td>

If the contact for the app has changed, enter the **First name**, **Last name**, and **Email** address for the new requester of the updated branded application.

</td></tr><tr><td>

**Your app's info** section

</td><td>

When you’re updating a branded app, this information can't be changed.

 **Important:** If you must change these fields, you must request a new branded app.

</td></tr><tr><td>

**App name** section

</td><td>

When you’re updating a branded app, the **Short name** can't be changed.

 **Important:** If you must change the **Short name**, you must request a new branded app.

</td></tr><tr><td>

Mobile Application Management \(MAM\)

</td><td>

Whether you want to use a MAM vendor with your apps. For more information, see [Mobile application management \(MAM\) integration](../concept/sg-mam.md).

 To enable a MAM vendor, select the **Use Mobile Application Management** toggle.

</td></tr><tr><td>

Mobile Application Management vendor

</td><td>

Select one of the following MAM vendors from the list:

-   **Blackberry**
-   **Intune**
 This field is only visible if you select the **Mobile Application Management \(MAM\)** toggle.

</td></tr><tr><td>

End-user license agreement \(EULA\) and privacy policy

</td><td>

EULA and privacy policy options can be updated or changed.

 Select the toggle **Use ServiceNow's EULA and privacy policy** to turn on the default EULA and privacy policy.

</td></tr><tr><td>

EULA

</td><td>

URL where app users can view your custom end-user license agreement from the mobile app settings. This option only displays when you don’t select to use the default ServiceNow EULA.

</td></tr><tr><td>

Privacy policy

</td><td>

URL where app users can view your custom privacy policy from the mobile app settings. This option only displays when you don’t select to use the default ServiceNow privacy policy.

</td></tr><tr><td>

iOS Universal links/Instances used for deep links**Note:** If you're updating an iOS branded app, this option is named **iOS Universal links**. If you’re updating an Android branded app, this option is named **Instances used for deep links**.

</td><td>

This table shows all ServiceNow instances used for your organization. Select the instance URLs that you want to be built into your app as an iOS Universal link or as an Android deep link.

 If you must configure a link to a URL that isn't listed in the table, select **Add custom URL**, enter the URL, and then it's added to the table for selection.

 **Note:**

-   This functionality can only be edited when you submit a new branded app request or when you update a branded app.
-   If you’re updating an iOS branded app, you must download the Apple App Site Association \(AASA\) JSON file after you submit this request and install the file on all instances in the URL list.
To learn more about deep links and universal links, see [Mobile URLs](../concept/mobile-urls.md).

</td></tr><tr><td colspan="2">

**Login management**

</td></tr><tr><td>

Pre-populate instance

</td><td>

Turn on this toggle to build an instance URL into your branded app so end-users don't need to enter the instance URL during login. Enter a default app instance URL that is secure and uses Hypertext Transfer Protocol Secure \(`https://`\).

 **Note:**

-   This instance URL can only be added when you submit a new branded app request or when you update a branded app.
-   Don’t select this option if you’re using AppConfig to preconfigure a default instance URL through an EMM suite or an embedded MAM SDK app. For more information, see [AppConfig for Mobile Apps](../reference/appconfig.md).


</td></tr><tr><td>

Default app instance

</td><td>

Enter the secure default app instance URL.

 This field is only visible if you select the **Pre-populate instance** toggle.

</td></tr><tr><td>

Nickname

</td><td>

\(Optional\) Enter a nickname for the **Default app instance** URL that displays on the mobile app for your end-users.

 This field is only visible if you select the **Pre-populate instance** toggle.

</td></tr><tr><td>

Icons and splash screens configurations

</td><td>

When you’re updating a branded app, this information can't be changed.

 **Important:** If you must change these fields, you must request a new branded app.

</td></tr><tr><td>

Internal iOS app testers \(iOS only\)

</td><td>

If you’re updating an iOS public or private branded app, you can change the **First name**, **Last name**, and **Email** address of the tester.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

After you complete the request form and submit it, your ServiceNow instance builds the updated branded app. When it completes, you receive an email notification about the status of the build. A link is provided from where you can download the app file.

**Note:**

-   You can only submit one build at a time. You can’t submit another build until the current build is canceled, failed, or completed.
-   Check the following table for estimated times to build your updated branded app.

    |App operating system|Public distribution|Private distribution|
    |--------------------|-------------------|--------------------|
    |iOS|1 week approximately|2–4 weeks \*|
    |Android|1 week or less|1 week or less|

    \* Privately distributed iOS apps must be inspected by Apple's human reviewers and can take 2–4 weeks until they’re ready for testing. If you are on a tight timeline, submit your privately distributed Android app first so that you can test it while you submit and wait for the iOS app build to complete

-   ServiceNow can't expedite delivery timelines because they’re determined by Apple or Google.

## What to do next

After the build successfully completes, select one of the below topic links to test and publish your updated branded app.

-   **[Test and publish an updated Android app for private distribution](testpub-updat-and-app-priv.md)**  
After you have requested an updated Android branded mobile app for private distribution, perform these steps to test and publish it.
-   **[Test and publish an updated iOS app for private distribution](testpub-updat-ios-app-priv.md)**  
AFter you have requested an updated iOS app for private distribution, perform these steps to test and publish it.
-   **[Test and publish an updated Android app for public distribution](testpub-updat-and-app-pub.md)**  
After you have requested an updated Android app for public distribution, perform these steps to test and publish it.
-   **[Test and publish an updated iOS app for public distribution](testpub-updat-ios-app-pub.md)**  
After you have requested an updated iOS branded mobile app for public distribution, perform these steps to test and publish it.

**Parent Topic:**[Request, test, and publish a branded mobile app](../concept/request-test-pub-branded-mob-app.md)

