---
title: Configure confidentiality in GRC tables
description: You can create a confidentiality configuration record in your GRC tables.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Confidential records, Common GRC features, Governance, Risk, and Compliance]
---

# Configure confidentiality in GRC tables

You can create a confidentiality configuration record in your GRC tables.

## Before you begin

Before you begin the confidentiality configuration on your table, you must create three new columns in the table that you want to enable confidentiality in.

Role required: sn\_grc.admin.

|Type|Comments|Example column name|Description|
|----|--------|-------------------|-----------|
|Boolean|Confidential|u\_confidential|Flag that marks or unmarks whether a field is confidential.|
|List, Reference to sys\_user table|Allowed users|u\_allowed\_users|Field that contains the list of users who can access the confidential record.|
|List, Reference to sys\_user\_group table|Allowed groups|u\_allowed\_groups|Field that contains the list of user groups who can access the confidential record.|

For more information, see [KB1497382](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1497382).

## Procedure

1.  Navigate to **All** &gt; **GRC Administration** &gt; **Confidentiality Configuration** and click **New**.

2.  In the new confidential configuration form, fill in the fields that are required for enabling confidentiality for the GRC tables.

    For more information about the fields, see [Confidentiality configuration form](../reference/confidentiality-configuration-form.md).

    ![Confidentiality configuration record.](../image/confidential-configuration.png "Confidentiality configuration record")

3.  Click **Submit**.


## Result

Confidentiality is enabled for the GRC table that you selected.

-   **[Confidentiality configuration form](../reference/confidentiality-configuration-form.md)**  
The Confidentiality configuration form is used for the configuration of the confidential records for your GRC tables.

**Parent Topic:**[Confidential records](../concept/confidential-records.md)

