---
title: Import Intelligence in TISC
description: Use this feature to manually import threat intelligence data into the repository, enabling analysts to ingest the relevant information from external sources as needed.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Threat Intelligence Security Center, Security Operations]
---

# Import Intelligence in TISC

Use this feature to manually import threat intelligence data into the repository, enabling analysts to ingest the relevant information from external sources as needed.

The following formats are supported for importing threat intelligence data:

<table id="table_bsj_k55_bgc"><thead><tr><th>

Import Format

</th><th>

Description

</th><th>

Records Supported

</th></tr></thead><tbody><tr><td>

Import from structured file

</td><td>

Download the sample file using the Preview link, and upload your structured data in a compatible format such as CSV, XLS, or XLSX.

</td><td>

-   Observables
-   Indicators

</td></tr><tr><td>

Import from standard format

</td><td>

Supported file types includeSTIX 2.x JSON and MISP JSON formats.

</td><td>

-   **STIX 2.1**: Observables, Indicators
-   **MISP**: Observables

</td></tr><tr><td>

Import from raw text

</td><td>

Parse the input as raw text to import observables. The maximum character limit for the input is 10,000 characters.

</td><td>

Observables

</td></tr><tr><td>

Import from file \(unstructured\)

</td><td>

The application will automatically parse the uploaded file to extract observables.Supported file types: TXT, CSV, JSON, XLS, and XLSX.

</td><td>

Observables

</td></tr></tbody>
</table>For a better understanding of each import format and the types of records supported, refer to the Related Information section.

-   **[Import data using structured file](../task/import-data-using-structured-file.md)**  
Upload the structured data in the supported file formats such as CSV, XLSX or XLS.
-   **[Import data using standard format](../task/import-data-using-standard-format.md)**  
Upload the standard data in the supported file formats such as STIX 2.x JSON, MISP JSON.
-   **[Import data using raw text](../task/import-data-using-pasted-text.md)**  
Import the observables data by copying and pasting raw text or entering the free text.
-   **[Import data using unstructured file format](../task/import-data-using-unstructured-file.md)**  
Upload the data in an unstructured format supported using the file formats such as TXT, CSV, JSON, XLS, XLSX.

**Related topics**  


[Import data using structured file](../task/import-data-using-structured-file.md)

[Import data using standard format](../task/import-data-using-standard-format.md)

[Import data using raw text](../task/import-data-using-pasted-text.md)

[Import data using unstructured file format](../task/import-data-using-unstructured-file.md)

