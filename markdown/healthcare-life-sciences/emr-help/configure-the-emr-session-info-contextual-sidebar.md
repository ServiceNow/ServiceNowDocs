---
title: Configure the EMR session info contextual sidebar
description: Configure the EMR session info contextual sidebar in Workspace to manage the fields that display there.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the EMR session info contextual sidebar

Configure the EMR session info contextual sidebar in Workspace to manage the fields that display there.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **EMR Help** &gt; **Request Definitions**.

2.  Select the request definition for which you want to configure the contextual sidebar.

3.  In the Request configuration mappings related list, use the Order column to sort the field order for the contextual sidebar.

    The lowest numerical value always displays first on the sidebar. So, for example, if email address has a value of 210 and phone number has a value of 200, you can swap those values to get phone number to display before email address.

    If a source system is defined in the request, then only the parameters for that source system will be displayed in the contextual sidebar based on their sort order. If no source system is defined in the request, then all parameters will display on the contextual sidebar.


