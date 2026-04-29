---
title: FTP data source extended properties
description: Certain properties are available for customizing your FTP data source.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# FTP data source extended properties

Certain properties are available for customizing your FTP data source.

To enter these properties, you must [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) the Data Source form and add the **Properties** field. When specifying more than one property, use a comma to separate each property.

<table id="table_rby_nqb_z3b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

connection.timeout

</td><td>

Defines the number of milliseconds to wait before timing out the FTP connection attempt.-   Default value: 10000
-   Example custom value: connection.timeout=12000
-   Data source: FTP, FTPS

</td></tr><tr><td>

remove\_file

</td><td>

Determines if the remote file is deleted after the import.-   Default value: true
-   Example custom value: remove\_file=false
-   Data source: FTP, FTPS, SFTP

</td></tr><tr><td>

rename\_file

</td><td>

Determines if the remote file is renamed after the import. Renamed files use the format &lt;original file name&gt;.imported.-   Default value: false
-   Example custom value: rename\_file=true
-   Data source: FTP, FTPS, SFTP

</td></tr></tbody>
</table>