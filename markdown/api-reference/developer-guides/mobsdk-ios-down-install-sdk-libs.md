---
title: Download and install the Mobile SDK libraries
description: Before you are able to create mobile applications that interact with your ServiceNow instance, you must first download and install the ServiceNow Mobile SDK libraries.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Get started with Mobile SDK - iOS, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Download and install the Mobile SDK libraries

Before you are able to create mobile applications that interact with your ServiceNow instance, you must first download and install the ServiceNow Mobile SDK libraries.

## Before you begin

Role required: none

Before you start the download and installation process, ensure that your development environment meets the following minimum requirements:

-   ServiceNow instance must be Washington DC or later.
-   iOS version must be 16.0 or later.

## Procedure

1.  In your development environment, create a folder alongside the rest of your application code in which to download the Mobile SDK iOS library.

    It is a good practice to create a folder named `vendor` in the root of your project’s location on the file system and download the unzipped Mobile SDK folder into that folder. It is also a good practice to check the SDK contents into your repository. This allows for a portable codebase and makes any accidental change to the SDK highly visible.

2.  Download the Mobile SDK iOS library, called NowKit from the ServiceNow Store.

    You can find the iOS libraries in the following locations:

    -   Mobile SDK: [https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/52821846803120101040fe43e5b9ee8c](https://store.servicenow.com/sn_appstore_store.do#!/store/application/52821846803120101040fe43e5b9ee8c)
    -   iOS library: [https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/1539a1f087ea3014970e2178cebb3564](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1539a1f087ea3014970e2178cebb3564)
    For details on installing applications on your instance, see [Administering applications](https://www.servicenow.com/docs/access?context=administering-applications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

3.  Navigate to the packaged\_sdk folder and unzip the `NowKit.zip` file which contains the NowSDK libraries.

    **Note:** It is important not to edit any ServiceNow Mobile SDK files or file structure. If you are experiencing issues with the SDK, open a support issue through your standard ServiceNow support process.


