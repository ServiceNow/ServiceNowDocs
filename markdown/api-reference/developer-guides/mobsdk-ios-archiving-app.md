---
title: Archive your application for publishing
description: It is important to disable rebuild from bitcode when archiving your application for publication for release.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Archive your application for publishing

It is important to disable **rebuild from bitcode** when archiving your application for publication for release.

To disable rebuild from bitcode, either set **ENABLE\_BITCODE** to `NO` in your project settings or clear the **Rebuild from Bitcode** check box when using Xcode to distribute your application.

![Xcode rebuild bitcode screen](../image/mobile_sdk-ios-rebuild-bitcode.png)

