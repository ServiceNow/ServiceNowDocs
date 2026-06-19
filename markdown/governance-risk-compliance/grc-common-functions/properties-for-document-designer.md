---
title: Reference information for Document designer
description: There are several properties that get installed with the Document designer plugin. These properties help to control the various aspects of how the plugin works.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/properties-for-document-designer.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install the add-in, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
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

Image types processed by the plugin and inserted into the Word document. The supported image types are: png, jpg, jpeg, and gif.

</td></tr><tr><td>

com.snc.word\_doc\_api.disable\_wordapi

</td><td>

Option to disable the API. When set to true, the API does not work. The default value is false.

</td></tr><tr><td>

com.snc.word\_doc\_api.image\_size\_limit\_kb

</td><td>

Maximum image size in kilobytes. If the image exceeds this value, the plugin stops processing and returns a status failure with an error message. The default value is 100.

</td></tr><tr><td>

com.snc.word\_doc\_api.max\_repetitions

</td><td>

Number of times a repeater block is duplicated and inserted consecutively into the Word document. The default value is 500.

</td></tr></tbody>
</table>**Parent Topic:**[Install the ServiceNow Document Designer add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/install-document-designer.md)

