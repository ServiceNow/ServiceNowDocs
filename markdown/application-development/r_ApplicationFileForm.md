---
title: Application File form
description: Use the Application File form to view relationships between applications and configuration records.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application files, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application File form

Use the Application File form to view relationships between applications and configuration records.

|Field|Description|
|-----|-----------|
|Display name|Display name for the configuration record.|
|Update name|Unique identifier for the configuration record. This value is used to identify versions and updates of the record.|
|Class|Table that contains the configuration record.|
|Application|Application that contains the configuration record.|
|Protection policy|Policy that determines if the configuration record is protected from changes. See Protected Application Files.|
|Created|Creation date of the configuration record.|
|Created by|User who created the configuration record.|
|Updated|Last update date for the configuration record.|
|Updated by|User who last updated the configuration record.|
|Related Record Versions|Version records for the related configuration record. A version record is created every time a user changes the related record. Use this list to compare versions of the configuration record or to revert to a previous version. See Versions.|
|Related Record Updates|Local update records for the related configuration record. An update record is created for the most recent change to the related record in a given Update Set. See Update Sets.|

**Note:** You may find it useful to manually add an **Owned By** \(owned\_by\) field to this form. It indicates, for each application, who in IT owns the application and is responsible for maintaining information about it. The Data Certification function uses this field to send certification tasks every quarter, or at any time interval that is configured. You can assign certification tasks to other users, but using this field limits configuration effort. To learn more about adding a field to a form, and about Data Certification, see [Using the form designer](https://www.servicenow.com/docs/access?context=c_FormDesign&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Data Certification](https://www.servicenow.com/docs/access?context=c_DataCertification&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

