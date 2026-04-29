---
title: Data privacy overview
description: The Overview homepage is a starting point to manage your data and data privacy compliance.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data privacy, Data Privacy, Platform Privacy]
---

# Data privacy overview

The Overview homepage is a starting point to manage your data and data privacy compliance.

The Overview dashboard reports the current state of data classifications and anonymization jobs within your instance. You can view your data with the Overview dashboard to see how much data can be classified, the data classes available, the amount of data in each class, and more.

**Note:** Some classified data is broken into different categories. Selecting a sub-category in any chart will add or remove the category from the overall chart and adjust the counts.

![Displays the data privacy overview page.](../image/dps-overview.png)

## Basic metrics

You can view several basic privacy metrics at the top of the display.

![Basic metrics](../image/dps-basic-metrics.png)

|Metric|Description|
|------|-----------|
|Records anonymized by job|Data in tables and column in the instance anonymized using job and user based anonymization policies.|
|Real time records anonymized|Data in transit \(via tables/columns and real-time channels\) to the instance, anonymized using real-time anonymization policies\).|
|Alert submissions|Notifications provided to users when sensitive data is detected in a field.|
|Blocked submissions|Data entry submissions prevented due to sensitive data blocking policies.|
|Quarantined attachments|Attachments containing sensitive data that have been isolated from the system for security review.|

You can choose to sort the information with the time dropdown, to any of the following views:

-   Last 7 days
-   Last 30 days
-   Last 90 days
-   All time

Select **View more data** underneath any metric to review it in more detail.

## Data classification

Displays information on data records.

![Data classification](../image/dps-data-classification.png)

<table id="table_pd2_sdm_k3c"><thead><tr><th>

Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Classifiable data

</td><td>

-   The total number of data records in the instance that can be classified.
-   The number is broken down into the total number of classified data and the total of unclassified data.
-   Gives administrators a quick view of potential classification opportunities.

</td></tr><tr><td>

Classified data

</td><td>

-   The total number of data records in the instance that have been classified.
-   The number is broken down into the total number of classified data for each assigned data class.
-   Provides a quick understanding how much data has been classified in each area.

</td></tr></tbody>
</table>## Data anonymization

You can track anonymization methods applied to protect data.

**Note:** The metrics displayed here apply to real-time anonymization and job-based anonymization when the [data pattern anonymization technique](../task/dps-create-anonymization-techniques.md) is selected. Both real-time anonymization and data pattern anonymization configurations make use of active data patterns, as defined in **ALL &gt; System Security &gt; Data Discovery \(Classic\) &gt; Active Data Patterns**.

![Data anonymization](../image/dps-data-anonymization.png)

Each metric provides the following information on its data pattern:

-   Total number of anonymizations for this data pattern
-   The number of real time anonymizations for this data pattern
-   The number of job-based anonymizations for this data pattern

You can choose to sort the information with the time dropdown, to any of the following views:

-   Last 7 days
-   Last 30 days
-   Last 90 days
-   All time

## Alerting and blocking

You can track top alert and blocked data patterns.

![Alerting and blocking](../image/dps-alerting-blocking.png)

The chart shows the most frequently detected types of sensitive information found during data discovery scans. It shows whether the information was alerted or blocked.

You can choose to sort the information with the time dropdown, to any of the following views:

-   Last 7 days
-   Last 30 days
-   Last 90 days
-   All time

## Other resources

For additional information on how to get started securing your instance with data privacy, you can access additional product learning resources about classification or anonymization on the right, including links to videos, documentation, and FAQs.

