---
title: Create a Firebase account
description: Create a Google Firebase project and enable the Google Vision API.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure photo search, Mobile photo search, Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a Firebase account

Create a Google Firebase project and enable the Google Vision API.

## Before you begin

Role required: admin

Photo search requires a Google Cloud / Firebase account to analyze images and return search results. If you already have a Google account, you can use your existing account. If not you can create an account at [https://firebase.google.com/](https://firebase.google.com/).

**Note:** Configuration for your Firebase account includes upgrading your account to the Blaze plan. This plan is a billable service that you must configure with Google.

## Procedure

1.  Navigate to [Firebase](https://firebase.google.com/) website, and sign in with a new or existing Google account.

2.  Click **Create Project**.

3.  Give your project a name and continue through the guided steps. The Firebase project page appears once you have completed the project setup.

4.  From the project setup page, add an iOS or Android app to your project by selecting the **iOS** or **Android** button.

    ![The Firebase homepage with highlighted iOS and Android buttons.](../image/firebase-add-app.png)

5.  In the **App setup** page, fill in the form to add an app to your Firebase project.

    1.  Enter a **bundle ID** and **App nickname** for your app. There are no specific requirements for the bundle ID and app nickname fields.

    2.  You do not need to download the configuration file, add an Firebase SDK, add an initialization code, or run your app to verify installation. You can click **Next** or **Skip this step** to bypass these steps.

    After completing setup you can see the configuration page for your project, with your new application listed.

6.  Click the **Spark Plan** button.

7.  Select the Blaze plan.

    **Note:** The Blaze plan is a billable plan. For details on pricing see [Firebase pricing](https://firebase.google.com/pricing).

8.  When prompted, create a billing account and enter in your payment details.

9.  Navigate to the [Google Cloud Platform](https://console.cloud.google.com/) website.

10. Log in to the website using the same Google account used in the previous steps.

11. In the header, select the project you created in previous steps.

12. Use the **APIs &amp; Services** menu option to locate and enable the Google Vision API.

13. Return to the [Firebase](https://firebase.google.com/) website, and open your project settings page.

14. In another browser tab or window, log in to your ServiceNow instance.

15. Navigate to **System Mobile** &gt; **Mobile Branding** &gt; **Mobile App Configs**, and select the record for the mobile app where you want to configure photo search.

16. In the **Vision iOS App ID** field, enter the App ID for your iOS app listed on your Firebase project settings page.

17. In the **Vision Android App ID** field, enter the App ID for your Android app listed on your Firebase project settings page.

18. In the **Vision API Key** field, enter the Web API Key listed on your Firebase project settings page.

19. Click **Update**.


**Parent Topic:**[Configure photo search](sg-configure-image-search.md)

