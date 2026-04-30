---
title: Scheduled jobs for Microsoft 365
description: Your Microsoft 365 integration profile is set to fetch subscription and usage information automatically from the Microsoft 365 Admin Center on a schedule. If needed, you can also manually run the following scheduled jobs to get this information. Each job must be complete before starting the next one.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Scheduled jobs for Microsoft 365

Your Microsoft 365 integration profile is set to fetch subscription and usage information automatically from the Microsoft 365 Admin Center on a schedule. If needed, you can also manually run the following scheduled jobs to get this information. Each job must be complete before starting the next one.

|Sequence|Scheduled job|Run frequency|Description|
|--------|-------------|-------------|-----------|
|1|SAM - Import M365 User Subscriptions|Weekly|Imports user subscriptions data for each Microsoft 365 product into the Software Subscription \[samp\_sw\_subscription\] table.|
|2|SAM - Collect Microsoft 365 Usage|Daily|Collects usage data for each Microsoft 365 product in the Software Usages \[samp\_sw\_usage\] table.|
|3|SAM - Create New Reclamation Candidates for Office 365 Integration|Weekly|Generates removal candidates for Microsoft 365 and Office 365.|
|4|SAM - Microsoft 365 Daily Job|Daily|Populates charts based on the data available in the subscription table and reclamation candidate table.|

**Related topics**  


[Integrating with Microsoft 365](../concept/integrate-with-microsoft.md)

