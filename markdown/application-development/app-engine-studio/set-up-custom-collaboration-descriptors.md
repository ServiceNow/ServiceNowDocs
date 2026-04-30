---
title: Set up custom collaboration descriptors
description: Customize the set of development collaborators you list in App Engine Studio \(AES\) using Guided Setup.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform configuration tasks, Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Set up custom collaboration descriptors

Customize the set of development collaborators you list in App Engine Studio \(AES\) using Guided Setup.

## Before you begin

Role required: admin

## About this task

Owner and Editor collaboration descriptors are provided out of the box in AES and have special capabilities. Development permissions included in each descriptor can be configured to your platform needs. You can create custom descriptors as well, in the global scope, so they can be used in AES.

**Note:** You should create collaboration descriptors in addition to Owner and Editor in the global scope. If you want collaboration descriptors to appear and be used in AES, you should also set them to `standard = TRUE`. AES doesn't support collaboration descriptors that are created in custom scopes, and non-standard collaboration descriptors don't render in AES.

Admins or delegated developers who invite collaborators can use these descriptors to delegate different types of work.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio** &gt; **Guided Setup**.

2.  Select **Get Started**.

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button is labeled **Continue**.

3.  In the Set up user access section, select **Set up Collaboration Descriptors**.

4.  In the Set up Collaboration Descriptors section, select **Configure**

5.  Select **New**.

6.  Give the new app collaboration descriptor a name and description.

7.  Select **Submit**.


## What to do next

Further customize collaborator permissions in App Engine Studio. For more information, see [Change collaborator permissions](../concept/aes-collaboration-feature-overview.md#).

**Parent Topic:**[Perform AES configuration tasks](../reference/aes-config-tasks.md)

