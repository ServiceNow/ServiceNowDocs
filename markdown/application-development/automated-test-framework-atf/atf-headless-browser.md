---
title: Headless Browser for Automated Test Framework
description: Improve your UI testing by automating the creation of browsers to process Automated Test Framework \(ATF\) User Interface \(UI\) tests. This feature is known as a headless browser, and helps you test UI functionality without having to manually open a browser to the Client Test Runner, which is what processes the UI tests in your local browser.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Headless Browser for Automated Test Framework

Improve your UI testing by automating the creation of browsers to process Automated Test Framework \(ATF\) User Interface \(UI\) tests. This feature is known as a headless browser, and helps you test UI functionality without having to manually open a browser to the Client Test Runner, which is what processes the UI tests in your local browser.

**Important:** Headless Browser is a legacy feature of ATF; it is recommended to instead use the ATF Test Generator and Cloud Runner application. Cloud Runner offers you an easy setup and a seamless user experience. You can install [Cloud Runner](https://store.servicenow.com/sn_appstore_store.do#!/store/application/db1676d7421441106f046193880e0b37) from the store app.

If you are an on-premise instance user, you must continue using the Headless Browser option. Cloud Runner is not currently available for on-premise instances.

## Background

ServiceNow customers use Automated Test Framework \(ATF\) to test applications and instances. When developing in the ServiceNow platform, ATF ensures that your changes have both the desired behavior and don’t break existing features.

Since the ServiceNow Orlando release, customers can automate the testing and deployment of their applications via the [Continuous Integration/Continuous Delivery \(CI/CD\) API](https://www.servicenow.com/docs/access?context=cicd-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Overview of Headless Browser

The automation provided by the ServiceNow Headless Browser for ATF skips the step of manually opening a browser during testing. There are several sequential procedures to follow in the one-time setup. Below are the instructions for both Linux and Windows setup.

See [Headless Browser for ATF](https://github.com/ServiceNow/atf-headless-runner?tab=readme-ov-file#support-model) for more information on the Support Model.

-   **[Headless Browser setup for Linux](headless-browser-procedure-linux.md)**  
The ServiceNow® Headless Browser for Automated Test Framework provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Linux.
-   **[Headless Browser setup for Microsoft Windows](headless-browser-procedure-windows.md)**  
The ServiceNow® Headless Browser for Automated Test Framework \(ATF\) provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Windows.
-   **[Headless Browser system properties](../reference/atf-headless-browser-properties.md)**  
Below is a table of the properties you must have as you set up the ServiceNow® Headless Browser for Automated Test Framework.
-   **[Headless Browser troubleshooting](headless-browser-troubleshoot.md)**  
These tips can help you troubleshoot your Linux or Microsoft Windows setup of the ServiceNow® Headless Browser for Automated Test Framework.

**Parent Topic:**[Automated Test Framework \(ATF\)](atf-landing-page.md)

