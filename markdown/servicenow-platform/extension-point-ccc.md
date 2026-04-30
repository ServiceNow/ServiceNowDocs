---
title: Extension points in Voice
description: Using extension points, you can call the custom scripts to extend the functionality of ServiceNow Voice. While integrating a third-party phone system with ServiceNow Voice, you can invoke extension points using the CTI API to handle events in ServiceNow Voice.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripting for operation handlers, Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Extension points in Voice

Using extension points, you can call the custom scripts to extend the functionality of ServiceNow Voice. While integrating a third-party phone system with ServiceNow Voice, you can invoke extension points using the CTI API to handle events in ServiceNow Voice.

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

To view the extension points that are available by default, navigate to **System Extension Points** &gt; **Scripted Extension Points** and group by the ServiceNow Voice application.

**Note:** You should install the ServiceNow Voice, ServiceNow Voice for ITSM, ServiceNow Voice for CSM, and ServiceNow Voice with Amazon Connect applications from the ServiceNow® Store. For information about these installations, see [Install ServiceNow Voice applications](../task/install-ccc-apps.md), [Install ServiceNow Voice for ITSM](../task/install-ccc-itsm.md), and [Install ServiceNow Voice for CSM](../task/install-ccc-csm.md).

|Extension point|Description|
|---------------|-----------|
|sn\_cti\_core.clickToCallContextMap|Enables the copying of application-specific field values to interaction records for ServiceNow Voice outbound calls.|
|sn\_cti\_core.CTICallAnalysisExtractor|Defines how the transcription and the recording data is retrieved for an interaction based on the third-party phone system integrated with ServiceNow Voice.|
|sn\_cti\_core.SoftPhoneEventSink|Defines if the third-party phone system can handle an event. Maps events from the Softphone interface to back-end events.|

**Parent Topic:**[Scripting for operation handlers](cloud-call-center-api.md)

