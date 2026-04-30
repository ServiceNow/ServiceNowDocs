---
title: Use CMDB groups to add OT context to IT CIs
description: Use Configuration Management Database \(CMDB\) groups to group IT configuration items \(CIs\) based on additional information, like installed software. Then you can add Operational Technology \(OT\) context to the IT CIs.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Use CMDB groups to add OT context to IT CIs

Use Configuration Management Database \(CMDB\) groups to group IT configuration items \(CIs\) based on additional information, like installed software. Then you can add Operational Technology \(OT\) context to the IT CIs.

## Before you begin

Role required: admin

## About this task

Using CMDB groups doesn't change the class of the IT CI. It instead adds OT entity records to the IT CI, which captures the OT context.

**Note:**

Follow these general guidelines:

1.  Ensure the filter conditions on the CMDB Group returns unique set of CI records every time. For example, adding a filter condition such as **OT device details is EMPTY** ensures that only records without OT device details are considered.
2.  Make sure the indexed fields are used as part of the filter criteria conditions. Ensure that the data set does not exceed 10,000 records to avoid performance related issues.

    **Note:** The CMDB Group API doesn't support retrieving records exceeding 10,000 or the limit defined by the following properties.

    -   glide.cmdb.query.max\_results\_limit
    -   glide.cmdb.group.max\_ci\_limit
    To address this, these properties need to be adjusted to allow for larger query results if the CMDB query contains more records than the current limits permit.

3.  Make sure to create an Automated IT to OT Bulk Conversion \(sn\_automated\_it\_ot\_bulk\_conversion\) record per CMDB Group to have filtering at a group level and define respective OT entity default values.
4.  Validate the data in the **OT Entity Default Configuration** tab. OT entity records are created using these default values.

## Procedure

1.  Define a CMDB group with the required filter criteria that identifies the right IT CIs..

    For more information, see [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

2.  Create an Automated IT to OT Bulk Conversion \(sn\_automated\_it\_ot\_bulk\_conversion\) record associated with the CMDB group.

    Creating this record adds OT context to IT CIs through the OT entity details.

    For more information about how to create an Automated IT to OT Bulk Conversion record, see [Automatically convert your IT records to OT devices](automatically-convert-it-records-to-ot-devices.md).

3.  To create a record in **sn\_automated\_it\_ot\_bulk\_conversion\_m2m\_cmdb\_group**, complete the following actions.

    1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Automated IT OT Bulk Conversion - Using CMDB groups**.
    2.  Select **New**.
    3.  In the **Automated IT to OT Bulk Conversion** field, select the record created in step 2.
    4.  In the **CMDB Group** field, select the CMDB created in step 1.
    5.  Select **Submit**.
    The record associates the CMDB group with the Automated IT to OT Bulk Conversion record.

    For example, if you want to add OT entity details for all computers that have a specific HISTORIAN software installed, we need to create a CMDB Group that matches this filter critieria. Then create a scheduled job and link it to the CMDB Group for computers that have HISTORIAN software installed.


**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

