---
title: Microsoft 365 Apps Usage Reports
description: Find the last activity date for Microsoft 365 products to determine reclamation candidates.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Microsoft 365 Apps Usage Reports

Find the last activity date for Microsoft 365 products to determine reclamation candidates.

The values for each field in the Microsoft 365 Apps Usage Reports \[samp\_m365\_apps\_usage\_report\] table are populated using the Microsoft Graph APIs. The **Last Activity Date** helps in determining reclamation candidates more accurately for the supported Microsoft 365 products, including Microsoft Outlook, Word, PowerPoint, Excel, Teams, and OneNote.

|Field|Description|
|-----|-----------|
|User Principal Name|Email address of the user.|
|Last Activity Date|Date the software product was last used.|
|Last Activation Date|Date on which the software product license was last activated for the user.|
|Report Period|Number of days for no meaningful activity before a user account is added to the list of reclamation candidates. The default value is 30 days.|
|Report Refresh Date|Date of the last refresh of the report.|
|Windows|Indicates usage of Windows with the value True or False.|
|Mac|Indicates usage of macOS with the value True or False.|
|Excel \(Mac\)|Indicates usage of Microsoft Excel on macOS with the value True or False.|
|PowerPoint \(Mac\)|Indicates usage of Microsoft PowerPoint on macOS with the value True or False.|
|Outlook \(Mac\)|Indicates usage of Microsoft Outlook on macOS with the value True or False.|
|Word \(Mac\)|Indicates usage of Microsoft Word on macOS with the value True or False.|
|OneNote \(Mac\)|Indicates usage of Microsoft OneNote on macOS with the value True or False.|
|Teams \(Mac\)|Indicates usage of Microsoft Teams on macOS with the value True or False.|
|Excel \(Windows\)|Indicates usage of Microsoft PowerPoint on Windows with the value True or False.|
|PowerPoint \(Windows\)|Indicates usage of Microsoft PowerPoint on Windows with the value True or False.|
|Outlook \(Windows\)|Indicates usage of Microsoft Outlook on Windows with the value True or False.|
|Word \(Windows\)|Indicates usage of Microsoft Word on Windows with the value True or False.|
|OneNote \(Windows\)|Indicates usage of Microsoft OneNote on Windows with the value True or False.|
|Teams \(Windows\)|Indicates usage of Microsoft Teams on Windows with the value True or False.|

**Parent Topic:**[Software Asset Management references](references.md)

