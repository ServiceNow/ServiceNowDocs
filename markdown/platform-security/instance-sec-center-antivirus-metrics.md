---
title: Antivirus metrics
description: If the Antivirus Scanning plugin is activated, Antivirus Scanning runs in your instance to help protect it against virus infections from attachments.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# Antivirus metrics

If the Antivirus Scanning plugin is activated, Antivirus Scanning runs in your instance to help protect it against virus infections from attachments.

The following metrics appear for the last 60 days of activity, and enable you to assess the effectiveness of the Antivirus Scanning functions.

## Antivirus Events

Antivirus Events indicate the number of antivirus events in your instance, by date. To access the antivirus events, navigate to **System Security** &gt; **Instance Security Center** and select the Metrics tab. Color coded graph lines represent the following types of antivirus events:

<table id="table_vdw_n25_yfb"><thead><tr><th>

Color

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blue

</td><td>

Number of files quarantined by Antivirus Scanning in this instance for the indicated date.

</td></tr><tr><td>

Green

</td><td>

Number of infected files downloaded to the instance, and then quarantined for the indicated date. These files are primarily email attachments that contain a virus or rouge code.

</td></tr><tr><td>

Yellow

</td><td>

Number of quarantined files in the instance that were deleted for the indicated date.

</td></tr><tr><td>

Orange

</td><td>

Number of quarantined files in the instance that were restored for the indicated date.**Note:** After Antivirus Scanning runs and finds any false positives, you can restore a quarantined file and make it accessible in the instance.

</td></tr></tbody>
</table>-   To access the Analytics Hub page and view the detailed score card and analytics information for a specific date, click a colored line in the Antivirus Events graph. For example, click the blue graphics line to view analytics information for files quarantined for a specific date.
-   To view the following breakdowns in the Analytics Hub page, click ![Breakdown icon](../image/Breakdown_icon.png), then click:

<table id="table_wvf_v5t_1jb"><thead><tr><th>

Breakdown

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AppSec - Antivirus Event Source

</td><td>

Source of the antivirus event.-   **On Upload:** Occurred due to an upload of an infected file, usually an attachment.
-   **From Quarantine:** Occurred due to the quarantine of an infected file, usually an attachment.
-   **On Download:** Occurred due to a download of an infected file, usually an attachment.
-   **From Record:** Occurred due to an infected record in a table.


</td></tr><tr><td>

AppSec - Antivirus Event Type

</td><td>

Type of antivirus event.-   **Quarantined:** Occurred due to the quarantine of a file, usually an attachment.
-   **Downloaded:** Occurred due to a download of a file, usually an attachment.
-   **Restored:** Occurred due to the restoration of a quarantined file.
-   **Deleted:** Occurred due to the deletion of a quarantined file.


</td></tr><tr><td>

AppSec - Antivirus Uploader

</td><td>

Name of the logged in user who uploaded the files that were the source of virus infections detected by the Antivirus Scanning application.

</td></tr></tbody>
</table>
## Quarantined Files

Lists the infected files in the instance quarantined by Antivirus Scanning:

|Field|Description|
|-----|-----------|
|File name|Name of the infected file.|
|Content type|Type of content that was infected in the file. For example, **application/x-dosexec** is an infected application or DOS executable file, while **text/plain** is an infected .txt file.|
|Table|Name of the table that contains the infected file. For example, **incident** appears for an incident file record.|
|Virus|Name of the file quarantined by Antivirus Scanning.|
|Detected|Date and time the infected file was detected.|
|Created By|Name of the user who quarantined the infected file.|
|Created|Date and time the quarantine file record was created.|
|Table sys ID|Table system identifier assigned to the quarantine file record.|

**Note:** You can also add **Quarantined Files** and **Virus Types** tiles to the Event ribbon. To learn more, see [Monitor security events](instance-sec-center-event-ribbon.md) and [Configure the security event ribbon](../task/instance-sec-center-configure-event-ribbon.md).

**Parent Topic:**[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

**Related topics**  


[Antivirus Scanning](antivirus-protection.md)

[Configuring Antivirus Scanning](../task/configure-antivirus-protection.md)

[Reviewing quarantined files](../task/resolve-infected-file.md)

[Reviewing antivirus activity](../task/generate-log-report-of-quarantined-files.md)

[Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

[Performance Analytics breakdowns](https://www.servicenow.com/docs/access?context=c_CreatingBreakdowns&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

[Analytics, Intelligence, and Reporting](https://www.servicenow.com/docs/access?context=c_performanceAnalyticsAndReporting&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

