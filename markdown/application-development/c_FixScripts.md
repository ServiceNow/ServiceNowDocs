---
title: Fix scripts
description: A fix script is server-side JavaScript code that you run after an application is installed or upgraded.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Fix scripts

A fix script is server-side JavaScript code that you run after an application is installed or upgraded.

Include fix scripts to make changes that are necessary for the data integrity or product stability of an application.

Administrators can create, manage, and run fix scripts. Users with the script\_fix\_admin role can create and manage fix scripts but cannot run fix scripts.

**Note:** An annotation with the following message shows up when you open an existing fix script or create a new fix script.![Image showing the annotation "Any customizations you make to the fix script will apply only when you manually run the script. Instance upgrades use the out of box fix script"](../image/uc-fixscript-annotation.png)

