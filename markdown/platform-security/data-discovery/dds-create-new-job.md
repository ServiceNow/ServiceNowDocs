---
title: Create discovery job
description: Create and schedule a new Data Discovery Store job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/dds-create-new-job.html
release: brazil
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Data Discovery scheduled discovery, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Create discovery job

Create and schedule a new Data Discovery Store job.

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Scheduled Discovery**.

2.  Select **Discovery Jobs** in the right side navigation pane.

3.  Fill in the form.

<table id="table_qqp_lgg_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the job.

</td></tr><tr><td>

Description

</td><td>

Description of the job.

</td></tr><tr><td>

Scan Type

</td><td>

Number of entries to be scanned. Possible states are as follows:-   **Sample**: Scans 10,000 entries.
-   **Full**: Scans all entries.
-   **Incremental**: Scans new or modified records or configurations.


</td></tr><tr><td>

Select policy

</td><td>

The policy to use for the scheduled job.

</td></tr><tr><td>

Start Date

</td><td>

Sets the start date for the job.

</td></tr><tr><td>

Time window start

</td><td>

The start of the time window to run this job. The job will run after the time entered in this field. The time entered in the **Time window start** field must happen before the time entered in the **Time window end** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr><tr><td>

Time window end

</td><td>

The end of the time window to run this job. The job runs until the time entered in this field. If the job hasn't complete this time, the job pauses and resumes at the next time window start. The time entered in the **Time window end** field must happen after the time entered in the **Time window start** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr></tbody>
</table>4.  Select additional options for your job:

    Depending on the selected Scan Type you've chosen, you can choose from the following optional checkbox options to further define your discovery job:

<table id="table_gk4_kbc_ckc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scan attachments

</td><td>

Scan file attachments that are not strictly image files.**Note:** You can view the attachments which contain sensitive data by selecting **Attachment Findings** in the **Scheduled Discovery** menu,

The following file types are supported when scanning attachments: PDF, DOC\(X\), TXT, XLS\(X\), CSV, XML, EML, MSG, JPG, JPEG and PNG.

**Warning:** This feature requires sending your data to a controlled ServiceNow environment. Contact your account and support teams for enabling the attachment scanning feature

</td></tr><tr><td>

Track granular findings

</td><td>

Show the specific records that contain sensitive data. Enabling this option may increase job run times.**Note:** You can see these results in the job details after the job completes, by selecting the **Data Discovery Granular Findings** tab.

</td></tr><tr><td>

Scan embedded images

</td><td>

Scans standalone images \(for example, PNG or JPG files\) and images embedded within documents \(such as scanned PDFs or Word files with image attachments\). Enabling this may increase scan duration significantly depending on the number of documents and images.**Note:** You can view the images which contain sensitive data by selecting **Attachment Findings** in the **Scheduled Discovery** menu,

</td></tr></tbody>
</table>5.  Select the **Schedule** button.


