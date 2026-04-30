---
title: Reference information for Document designer
description: There are several properties that get installed with the Document designer plugin. These properties help to control the various aspects of how the plugin works.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install the add-in, Configure document templates using Document Designer, Common GRC features, Governance, Risk, and Compliance]
---

# Reference information for Document designer

There are several properties that get installed with the Document designer plugin. These properties help to control the various aspects of how the plugin works.

<table id="table_kf4_nqk_qjb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.word\_doc\_api.size\_limit\_mb

</td><td>

This property restricts the size of contract documents in mega bytes. The default value is 5.

</td></tr><tr><td>

com.snc.word\_doc\_api.unzip\_word\_size\_limit\_mb

</td><td>

This property restricts the size of unzipped Word documents in mega bytes. The default value is 10.

</td></tr><tr><td>

com.snc.word\_doc\_api.supported\_image\_types

</td><td>

This property ensures that only the image types specified in the property will be processed by the plugin and inserted into the Word Document. The supported image types are: png, jpg, jpeg, and gif.

</td></tr><tr><td>

com.snc.word\_doc\_api.disable\_wordapi

</td><td>

This property ensures that the API will not work if the property is set to true. The default value is false.

</td></tr><tr><td>

com.snc.word\_doc\_api.image\_size\_limit\_kb

</td><td>

This property ensures that if the image size in KB is more than the property value, the plugin will not start processing and will result in status failure with an error message. The default value is 100.

</td></tr><tr><td>

com.snc.word\_doc\_api.max\_repetitions

</td><td>

This property sets the number of times a repeater block \(a defined section of content\) will be duplicated and inserted consecutively into the Word document. Each repetition adds a new instance of the block immediately following the previous one, creating a sequential chain of repeated sections. The default value is 100.

</td></tr></tbody>
</table>