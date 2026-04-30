---
title: Defining Name Formats
description: The name format automatically generates a name for a document revision by arranging name components in a standard code to match naming conventions.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defining Document Parameters, Features, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Defining Name Formats

The name format automatically generates a name for a document revision by arranging name components in a standard code to match naming conventions.

For example, a name format with the name components **Type Code**, **Document Name**, and **Revision Number** and the separator **-**, would be formatted as:

`TYPECODE-Name-RevNumber.fileformat`

In this example, a policy \(code POL\) named `IT Off-Boarding Policy`, with revision number **1.0**, and uploaded as a **.docx** file would have the name:

`POL-IT Off-Boarding Policy-1.0.docx`

To define a new name format, navigate to **Managed Documents** &gt; **Administration** &gt; **Name Formats** and click **New**.

|Field|Description|
|-----|-----------|
|Name|A unique name for the name format.|
|Separator|A separator to put between each of the components. Hyphens \(-\) and underscores \(\_\) are commonly used. Using alphanumeric characters can create a confusing name format.|
|Description|A description of the name format.|

Use the related list to add name components. Use the **Order** field to set the sequence in which name components are used.

The following name formats are defined in the base system.

|Name|Separator|Description|
|----|---------|-----------|
|Default|\_|The default format. Document name and revision separated by an underscore.|
|Default Policy|\_|The format for the policy document type.|
|Development documentation|\(no separator\)|The format for the software documentation type.|
|Development Sources|\(no separator\)|The format for the development and code sources type.|
|Intranet Improvement|\(no separator\)|The format for documents that describe intranet use.|

**Parent Topic:**[Defining Document Parameters](r_DefiningDocumentParameters.md)

