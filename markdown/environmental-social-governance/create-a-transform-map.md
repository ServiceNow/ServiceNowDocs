---
title: Create a transform map
description: Create a transform map to match the columns from the staging table to the columns in the target table. The transformation helps to convert the data from the source table into metric data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Watershed, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a transform map

Create a transform map to match the columns from the staging table to the columns in the target table. The transformation helps to convert the data from the source table into metric data.

## Before you begin

If you already have manual Metric Definition in the system before the import, you must change the type of metric definition to **Automated** and the method type to **External source**.

​Role required: sn\_esg.program\_manager

## About this task

A map is transformed when you import data from a staging table such as Watershed Data \[sn\_esg\_watershed\_data\] to a target table such as Metric Data \[sn\_grc\_metric\_metric\_data\]. By default, there are three transform maps available for each table when you import data from Watershed.

## Procedure

1.  Navigate to **Operational Sustainability Management** &gt; **Watershed** &gt; **Import Sets**.

2.  Open the import set that you created.

3.  Under Related Links, select **Transform**.

4.  On the Specify Import Set and Transform map form, move the required maps from the **Available** column to the **Selected maps run in order** column.

5.  Select **Transform**.


**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Watershed](../concept/integrate-esg-with-watershed.md)

