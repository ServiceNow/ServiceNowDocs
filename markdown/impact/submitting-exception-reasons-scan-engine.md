---
title: Submit exceptions for the Scan Engine findings
description: For Recommend level findings, developers can submit exception requests if they feel the issue should not be considered a finding.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Submit exceptions for the Scan Engine findings

For Recommend level findings, developers can submit exception requests if they feel the issue should not be considered a finding.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

Generally, exceptions require approval from a system administrator. However, certain settings configured by a system administrator may determine if the exception is automatically approved or rejected.

## Procedure

1.  From the finding \(sn\_se\_finding\) record, locate the **Scanned Record** field.

2.  Select **Scan Engine Exceptions**.

    The sn\_se\_finding record must be extending the sys\_metadata table in order for the Scan Engine Exceptions button to be available.

    This displays all applicable script issues identified by the Scan Engine that also qualify for an exception.

3.  Enter the reason in the **Exception Reason** field for why an exception should be made for this finding.

4.  Select **Request Approval** to have the exception reviewed by a system administrator.

    If enabled, the exception state is Requested. If not, the state is Not Yet Requested.

5.  Select **OK** to submit the exception request.

    Once the exception request is saved, the applicable warning messages changes color as blue.


## What to do next

For more information on configuring exception properties, refer to [Configure exception reason properties](../task/exception-reason-properties.md).

