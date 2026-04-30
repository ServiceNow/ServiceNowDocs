---
title: Exploring Data Discovery
description: Use Data Discovery to identify sensitive data within an instance, such as credit card information, emails, or social security numbers.
locale: en-US
release: yokohama
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Discovery, Platform Privacy]
---

# Exploring Data Discovery

Use Data Discovery to identify sensitive data within an instance, such as credit card information, emails, or social security numbers.

Data Discovery runs a user-defined set of jobs on a set of tables. The jobs search for and report sensitive information for review on the Data Discovery dashboard. A scheduled job automatically uses all active data patterns and target tables when it runs.

Data Discovery also includes pre-allocated roles with varying levels of access to data.

## Access the Data Discovery dashboard

Navigate to **All** &gt; **System Security** &gt; **Data Discovery \(Classic\)** &gt; **Dashboard** to view the Data Discovery Dashboard and to review your current job findings.

![The Data Discovery Dashboard.](../image/data-discovery-dashboard.png "Data Discovery Dashboard")

## Discovered Data Patterns

**Tip:** Select a record to view more information and take further action with the findings. See [Data Discovery job results](data-discovery-findings.md#) for more.

The Discovered Data Patterns chart displays the number and percentage of currently discovered data patterns. Select a section to take further action.

## Data Discovery Findings by Status

The Data Discovery Findings chart reviews the number and percentage of currently discovered data patterns by their status.

## Discovered Tables

The Discovered tables highlight which tables currently discovered data is in, and their data pattern.

## Columns with Discovered Data

The Columns with Discovered Data section reviews currently discovered data by their column.

