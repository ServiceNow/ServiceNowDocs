---
title: Configuring Antivirus Scanning
description: Configure Antivirus Scanning across your instance and at the table level.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Antivirus Scanning]
---

# Configuring Antivirus Scanning

Configure Antivirus Scanning across your instance and at the table level.

## Before you begin

Role required: antivirus\_admin or admin

## About this task

Antivirus Scanning is active by default in your instance, where it automatically scans attachments to identify any files that are infected by viruses. Configure the feature by ensuring the scan is enabled across your instance, and by identifying any tables that you want to exclude from the scan.

## Procedure

1.  Navigate to **All** &gt; **Antivirus** &gt; **Configuration**.

2.  As you configure the feature, consider the following.

<table id="choicetable_ezd_bvf_2gb"><thead><tr><th align="left" id="d121625e80">

Option

</th><th align="left" id="d121625e83">

Description

</th></tr></thead><tbody><tr><td id="d121625e89">

**Enable Antivirus scanning**

</td><td>

Antivirus scanning is active and enabled on the instance by default, its toggle is set to the on position and appears green. **Note:** To set the property to be `false` contact customer support.

</td></tr><tr><td id="d121625e106">

**Allow attachments to be downloaded when Antivirus scanner is unavailable**

</td><td>

If this option is set to the on position, antivirus scanning is bypassed if the scanner times out, and a response can’t be obtained. In this situation, the file download proceeds without completing the scan. If the option is set to off, the file download is prohibited until the scan can complete successfully.

</td></tr><tr><td id="d121625e115">

**List of Tables Excluded**

</td><td>

Any file attachments associated with a table in this list are excluded from antivirus scanning. Proceed to Step 4 if you want to define the tables the system excludes from scanning.

</td></tr></tbody>
</table>3.  Select **Save**.

4.  Exclude tables from the Antivirus scan by adding them to the **List of Tables Excluded**.

    1.  Navigate to **System Definition** → **Dictionary**

    2.  Search for the table you want to exclude from the scan and select the table with Type set to collection.

    3.  In the **Attributes** tab, select **New**.

    4.  Add `Exclude_from_antivirus_scan` in the Attributes field and enter `True` in the **Value** field.

    5.  Select **Submit**.


## Result

Antivirus Scanning is enabled in your instance, and the **List of Tables Excluded** on the Antivirus Configuration page is populated with all the tables that you excluded from the scan.

