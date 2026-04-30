---
title: Configure application export functionality in Grants Management
description: Configure the export to PDF functionality so that grants program can export grants proposals directly to PDF.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure application export functionality in Grants Management

Configure the export to PDF functionality so that grants program can export grants proposals directly to PDF.

## About this task

The export application function generates a PDF format of the confirm application details involving the information from all the sections from the intake stage in sectional formatting.

PDF export functionality uses Document Templates table and a script to generate a PDF. However, these reside in different scopes, requiring RCA records to be created and manually allowed.

## Before you begin

Role required: admin

Verify that the scope is set to **Document Templates**.

**Note:** This may have configuration implications across all ServiceNow applications in your instance. Verify the RCA settings of other applications after completing this procedure.

## Procedure

1.  Navigate to **System Application** &gt; **Application Restricted Caller Access Privileges**

2.  Open the **Read** operation record and change the value of Status field to **Allowed**.

3.  In the Confirm Application Details activity, select **Export**.

4.  Open the **Execute API** operation record and change the value of Status field to **Allowed**.


## Result

The export PDF functionality should appear in the Confirm Application Details activity of the playbook.

## What to do next

The data that shows up in the exported PDF is generated based on a pre-configured document template. This configuration can be modified to add/delete fields, change formatting of the document, and more.

**Parent Topic:**[Configure Grants Management](psds-config-gmp-foundation.md)

**Previous topic:**[Configure a currency in Grants Management](psds-config-gmp-single-currency-setup.md)

**Next topic:**[Configure PaCE Eligibility Framework Engine for use with Grants Management](psds-config-gmp-pace.md)

