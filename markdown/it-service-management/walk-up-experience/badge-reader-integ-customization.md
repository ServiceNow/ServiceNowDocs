---
title: Customize badge Reader Integration
description: Badge Reader Integration includes several scripted extension points for you to customize script includes installed with the feature.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Customize badge Reader Integration

Badge Reader Integration includes several scripted extension points for you to customize script includes installed with the feature.

The underlying Badge Reader Integration script includes are read only. Customers who want to modify the look and feel of the feature can alter several script includes using scripted extension points.

Various scenarios exist whereby the ability to modify script-includes code is beneficial. For example, if you already use a data model to store your badge numbers, you may not want to use the Badge Reader Integration application User Badge \(sn\_badge\_user\_badge\) table to store your badge numbers. Instead, you can create an extension implementation for sn\_badge.BadgeReader that supports your data model.

Perhaps you want to customize the types of data you receive from a badge scan or how you want to parse that data. You can create an extension implementation for sn\_badge.BadgeReaderParser that supports your data model.

The following code is available for alteration using scripted extension points with the Badge Reader Integration application:

<table id="table_vbb_yf3_yjb"><thead><tr><th>

Scripted Extension Points

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BadgeReaderAPI name: sn\_badge.BadgeReader

</td><td>

Extension point used by the BadgeReaderImpl script includes.

 Use this script to find a badge reader by its device identifier.

</td></tr><tr><td>

BadgeReaderParserAPI name: sn\_badge.BadgeReaderParser

</td><td>

Extension point used by the BadgeReaderParserImpl script include.

 Use this to parse the card data string from the API.

</td></tr><tr><td>

BadgeReaderUserAPI name: sn\_badge.BadgeReaderUser

</td><td>

Extension point used by the BadgeReaderUserImpl script include.

 Use this script to find a sys\_user from a badge number and facility code.

**Note:** If you already have a data model for storing your badge numbers, this is the script to use to override the Badge Reader Integration application code to support your data model.

</td></tr><tr><td>

BadgeReaderScanProcessorAPI name: sn\_badge.BadgeReaderScanProcessor

</td><td>

Extension point used by the BadgeReaderScanProcessor script include.

 Use this frontage to manage the badge scan event.

</td></tr></tbody>
</table>For complete details about scripted extension points and how to create and use them, refer to [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) and [Creating and adding a scripted extension point](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-base-code&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](walkup-badge-read-integ-config.md)

