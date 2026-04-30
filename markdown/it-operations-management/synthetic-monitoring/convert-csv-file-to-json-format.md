---
title: Convert CSV file to JSON format
description: Convert your CSV file to JSON format to create synthetic monitors.
locale: en-US
release: zurich
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2026-02-18"
reading_time_minutes: 1
breadcrumb: [Use APIs to create synthetic monitor from terminal, Import synthetic monitors using API, Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Convert CSV file to JSON format

Convert your CSV file to JSON format to create synthetic monitors.

## CSV file to JSON format

To convert the CSV file to JSON format, access the terminal. Depending on your operating system, execute the required commands.

<table id="table_m1q_3jm_33c"><thead><tr><th>

Operating system

</th><th>

Curl commands

</th></tr></thead><tbody><tr><td>

macOS

</td><td>

`jq -Rs ‘{csv_content: .}’ filename.csv`

</td></tr><tr><td>

Windows Powershell

</td><td>

-   If using jq, use the command `jq -Rs ‘{csv_content: .}’ filename.csv`
-   If using only Powershell \(no jq installed\), use the commands:
    1.  `$csvContent = Get-Content -Path "synthetic_checks.csv" -Raw`
    2.  `$json = @{ csv_content = $csvContent } | ConvertTo-Json`
    3.  `$json`
-   If using Windows command prompt with jq installed, use the command `jq -Rs "{csv_content: .}" filename.csv`

</td></tr></tbody>
</table>The output is a CSV content wrapped in JSON format that is available on the terminal. `{ "csv_content": "name,method,description,interval,cmdb_ci,...\n\"Monitors1\",\"GET\",\"CHECK1\",5,..." }`

Once the content is available in JSON format, access the **Body** tab in Postman, and select **Raw** to paste the JSON format content and select **Send**.

**Note:** Ensure that the format selected is JSON.

The response status provides the job Id and the status of monitors created. If there are any errors found, fix the file and run the same commands to complete the monitor creation.

**Parent Topic:**[Create monitors in bulk using Terminal](bulk_monitor_creation_terminal.md)

