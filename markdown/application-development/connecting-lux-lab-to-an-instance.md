---
title: Connect Lux Lab to an instance
description: Connect Lux Lab to your ServiceNow instance so that you can access instance files, deploy changes, and preview your work. Instance sign-in is required before you can reach the app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/connecting-lux-lab-to-an-instance.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Connect Lux Lab to an instance, When to connect]
breadcrumb: [Configuring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Connect Lux Lab to an instance

Connect Lux Lab to your ServiceNow instance so that you can access instance files, deploy changes, and preview your work. Instance sign-in is required before you can reach the app.

## Before you begin

Role required: admin

Your machine meets the minimum system requirements. For the requirements, see [Configuring Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/configuring-lux-lab.md).

## About this task

On first launch, instance sign-in is the third and final step of the guided setup screen. You must complete it before you can reach the home page. You can also add or switch instances at any time after setup from the Instance Explorer.

## Procedure

1.  Start a new instance connection in one of the following ways:

    -   During first launch, go to the **Instance Sign-in** step of the guided setup.
    -   After setup, select the instance name in the top header bar, or open the **Instance Explorer** panel from the Activity Bar. In either case, select **Add Instance**.
2.  Enter your instance URL, including the protocol \(for example, `https://dev12345.service-now.com`\).

3.  Enter your instance user name and password.

    Lux Lab authenticates to the instance with basic authentication.

4.  Select **Connect**.


## Result

An indicator next to the instance name shows the connection status, as described in the following table.

|Indicator|Meaning|
|---------|-------|
|Green dot|Connected and responsive|
|Yellow dot|Connected but slow or degraded|
|Red dot|Connection failed or timed out|
|Gray dot|Disconnected|

## What to do next

After you connect, you can create an experience or browse instance tables from the Instance Explorer panel. For the procedure to create an experience, see [Create an experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-a-new-experience.md).

