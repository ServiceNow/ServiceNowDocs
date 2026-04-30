---
title: Configure Antivirus Scanning
description: Configure Antivirus Scanning across your instance and at the table level.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Antivirus Scanning

Configure Antivirus Scanning across your instance and at the table level.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Search for the table you want to exclude from the scan and select the table with Type set to collection.

3.  In the **Attributes** tab, select **New**.

4.  Add `Exclude_from_antivirus_scan`in the Attributes field and enter `True` in the **Value** field.

5.  Select **Submit**.


## Result

Antivirus Scanning is enabled in your instance, and the **List of Tables Excluded** on the Antivirus Configuration page is populated with all the tables that you excluded from the scan.

