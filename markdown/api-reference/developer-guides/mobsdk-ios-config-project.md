---
title: Configure your project
description: Before writing any application that leverages the Mobile SDK for iOS, you must configure your project to use the SDK.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Get started with Mobile SDK - iOS, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Configure your project

Before writing any application that leverages the Mobile SDK for iOS, you must configure your project to use the SDK.

## Procedure

1.  Add the Mobile SDK to your project.

    1.  In Xcode, drag the NowKit folder from Finder on to your Project Navigator pane \(⌘+1\). Xcode recognizes the folder as a Swift package and displays a folder icon next to **NowKit**.

        ![NowKit menu](../image/mobile_skd-ios-nowkit-menu.png)

    2.  Add the Mobile SDK to your target in the **Frameworks, Libraries, and Embedded Content** section of the project’s general settings by pressing the **+** icon and selecting the **NowKit** framework from the presented list.

        ![Target framework screen](../image/mobile_sdk-ios-target-framework.png)

2.  Update your project settings.

    The SDK uses several device features which require user permissions. You’ll need to add SDK feature grouped entries to your project’s Info.plist for the following keys:

    -   NowChat
        -   NSLocationWhenInUseUsageDescription
        -   NSLocationAlwaysAndWhenInUseUsageDescription
        -   NSMicrophoneUsageDescription
        -   NSSpeechRecognitionUsageDescription
    -   NowWeb
        -   NSCameraUsageDescription
        -   NSPhotoLibraryUsageDescription
    Ensure that you provide messages that are helpful to customers, such as the following:

    ```
    … 
    <key>NSCameraUsageDescription</key> 
    <string>[Your App] requires permission to access your camera to take attachment photos and scan barcodes.</string> 
    <key>NSPhotoLibraryUsageDescription</key> 
    <string>[Your App] requires permission to upload your photos to a record.</string> 
    …
    ```


