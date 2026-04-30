---
title: Installed with Software Spend Detection
description: User roles and tables are installed with Software Spend Detection. Demo data is available for Software Spend Detection.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Installed with Software Spend Detection

User roles and tables are installed with Software Spend Detection. Demo data is available for Software Spend Detection.

## User roles

|Role|Description|
|----|-----------|
|sam\_spend\_import|Role required to import financial transaction data into Software Spend Detection. Users with this role can view all modules in Software Spend Detection except **Content Service Setup**. Users with this role cannot view Software Asset Management.|

## Tables

|Table|Description|
|-----|-----------|
|Software Spend Transactions \[sam\_spend\_transaction\]|Financial transaction data.|
|Software Spend Transactions Import \[sam\_spend\_transaction\_import\]|Import summary table showing number of rows imported and any import errors.|
|Software Spend Transactions Import \[imp\_sam\_spend\_transaction\]|Staging table for financial transaction data imports.|
|Overlapping Software Configuration \[sam\_sw\_overlap\_configuration\]|List of reports shown on the Overlapping Software dashboard.|
|Overlapping Software Summary \[sam\_sw\_overlap\_summary\]|List of software products with spend transactions.|

**Parent Topic:**[Software Spend Detection](../concept/software-spend-detection.md)

