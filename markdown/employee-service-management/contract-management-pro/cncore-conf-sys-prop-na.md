---
title: Configure system properties for contract metadata extraction
description: Configure system properties to specify whether the contract metadata extraction should be automatically initiated or manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-conf-sys-prop-na.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring contract metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configure system properties for contract metadata extraction

Configure system properties to specify whether the contract metadata extraction should be automatically initiated or manually.

## About this task

The sn\_cm\_gen\_ai.cmpro\_initiate\_metadata\_extraction system property defines how the contract metadata extraction process is initiated on a contract repository record. By default, the system property is set to initiate the contract metadata extraction process manually.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## Procedure

1.  Navigate to the **All** menu and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  In the **Name** column, search for `sn_cm_gen_ai.cmpro_initiate_metadata_extraction`.

3.  Select the **sn\_cm\_gen\_ai.cmpro\_initiate\_metadata\_extraction** property.

4.  Update the **Value** field.

    -   To set manual initiation of the metadata extraction process, enter `manual`.
    -   To set automatic initiation of the metadata extraction process, enter `automated`.
    The default value is **manual**.

5.  Select **Update**.


**Parent Topic:**[Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction]()

[Map a use case for contract metadata extraction]()

[Enable notification for contract metadata extraction]()

[Configure the workspace URL for contract metadata extraction notifications]()

[Configure an extension point to add contract metadata]()

