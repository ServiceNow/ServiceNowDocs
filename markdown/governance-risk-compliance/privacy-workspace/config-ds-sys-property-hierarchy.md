---
title: Configure data subject selection in hierarchy relationships
description: Configure the sn\_privacy.relationship\_involving\_data\_subjects system property to enable data subject selection in custom hierarchy relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/config-ds-sys-property-hierarchy.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Configure data subject selection in hierarchy relationships

Configure the sn\_privacy.relationship\_involving\_data\_subjects system property to enable data subject selection in custom hierarchy relationships.

## Before you begin

Role required: sn\_privacy.admin

## About this task

By default, only certain built-in relationship types, such as **Sends data to** and **Received data from**, allow data subject type selection. The system property that controls which relationship types allow data subject selection is sn\_privacy.relationship\_involving\_data\_subjects. Update this record to extend the behavior to a custom relationship type.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the System Properties table, search for sn\_privacy.relationship\_involving\_data\_subjects, and open the record.

3.  In the **Value** field, enter the sys\_ID of the relationship type that should allow data subject selection.

    **Note:** The field accepts multiple sys\_ID values separated by commas with no spaces.

4.  To apply the change, select **Update**.


## Result

Business users or privacy analysts selecting the custom relationship type while defining hierarchy relationships are able to select data subject types, their locations, and impacted data elements.

**Parent Topic:**[Configuring Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-privacy-mgmt.md)

**Related topics**  


[Manage data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/data-transfers.md)

