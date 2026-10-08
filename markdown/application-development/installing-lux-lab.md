---
title: Install Lux Lab
description: Install Lux Lab on macOS or Windows from the ServiceNow Developer Store. On first launch, a guided setup takes you through environment, agent, and instance sign-in steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/installing-lux-lab.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Install Lux Lab]
breadcrumb: [Configuring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Install Lux Lab

Install Lux Lab on macOS or Windows from the ServiceNow® Developer Store. On first launch, a guided setup takes you through environment, agent, and instance sign-in steps.

## Before you begin

Role required: admin

You need a ServiceNow® developer account to sign in to the [ServiceNow Developer Store](https://developer.servicenow.com/).

Verify that your machine meets the minimum requirements in the following tables. The recommended specifications aren't required. However, the recommended specifications support running the dev server, agent chat, and preview panel simultaneously.

|Requirement|Minimum|Recommended|
|-----------|-------|-----------|
|OS version|macOS 12 \(Monterey\) or later|macOS 13 \(Ventura\) or later|
|Processor|Apple Silicon \(M1 or later\)|Apple Silicon M2 or later|
|RAM|8 GB|16 GB or more|
|Disk space|2 GB free|10 GB or more free|

|Requirement|Minimum|Recommended|
|-----------|-------|-----------|
|OS version|Windows 10 \(64-bit\) or later|Windows 11|
|Processor|Intel Core i5 or AMD Ryzen 5|Intel Core i7 or AMD Ryzen 7 or better|
|RAM|8 GB|16 GB or more|
|Disk space|2 GB free|10 GB or more free|

Lux Lab also requires the following:

-   Node.js v24 or later, for local build tooling
-   pnpm v10 or later, the recommended package manager
-   Git v2.30 or later
-   An active internet connection, for instance connectivity and agent features

## About this task

Download the Lux Lab app using the following link. [Lux Lab installation files](https://install.service-now.com/glide/distribution/builds/package/app-signed/aiux/Lux-Lab-official-release.zip).

## Procedure

1.  macOS

    1.  Download the Lux Lab `.dmg` installer using the following link.

        [Lux Lab installation files](https://install.service-now.com/glide/distribution/builds/package/app-signed/aiux/Lux-Lab-official-release.zip).

    2.  Open the `.dmg` file.

    3.  Drag Lux Lab into your `/Applications` folder.

    4.  If macOS displays a security prompt on first launch, select **Open Anyway** in **System Settings** &gt; **Privacy &amp; Security**.

        Lux Lab opens and prompts you to sign in.

2.  Windows

    1.  Download the Lux Lab `.exe` installer using the following link.

        [Lux Lab installation files](https://install.service-now.com/glide/distribution/builds/package/app-signed/aiux/Lux-Lab-official-release.zip).

    2.  Run the installer.

    3.  Follow the on-screen prompts.

    4.  When the installer completes, launch Lux Lab from the Start menu or the desktop shortcut.


## Result

Lux Lab is installed. On first launch, a guided setup screen takes you through three steps before you reach the app: Environment, Agents, and Instance Sign-in.

## What to do next

To complete setup, connect Lux Lab to your instance; this step is required, because you can't reach the app without it. For the procedure, see [Connect Lux Lab to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/connecting-lux-lab-to-an-instance.md).

